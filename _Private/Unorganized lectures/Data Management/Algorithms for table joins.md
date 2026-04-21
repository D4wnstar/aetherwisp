The most basic algorithm is a **nested loop** and is the default strategy when nothing better applies. Call $T_{1}$ and $T_{2}$ the two tables that your are joining. Consider $T_{1}$ to be the external table and $T_{2}$ the internal one. For each page $p_{1}$ of $T_{1}$, for each record $r_{1}$ of $p_{1}$, for each page $p_{2}$ of $T_{2}$, for each record $r_{2}$ of $p_{2}$, take $r_{1}\cdot r_{2}$ if the join condition is true. In pseudocode:

```julia
for p_1 in T_1
	for r_1 in p_1
		for p_2 in T_2
			for r_2 in p_2
				if join_condition(r_1, r_2) == true
					take(join(r_1, r_2))
				end
			end
		end
	end
end
```

Needless to say, this is an incredibly expensive algorithm, since there are four (!) nested loops. It is fine for small tables that can entirely fit in a memory buffer and maybe surprisingly the most performant one when one of the two tables is almost-empty tables (1 or 2 records) since it has no overhead and the lack of records effectively deletes two loops.

A more practical algorithm is the **indexed nested loop**, which is available if an index is defined for the join attribute of the internal table. The idea is, for each row in the external column, extract the join attribute, then search the internal table for all records matching the attribute using the index. In pseudocode:

```julia
for p_1 in T_1
	for r_1 in p_1
		found_records = index_search(T_2, join_attr(r_1))
		for r_2 in found_records
			take(join(r_1, r_2))
		end
	end
end
```

Another algorithm is the **merge join**. This is used for data that is physically ordered (as in, the records are ordered on disk) and has good performance. Ordering is with respect to the primary key for the external table and to the foreign key for the internal table.