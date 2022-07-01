# Best merge

Merge rows of a table.


## Problem

We have a database table as below:

		C1  C2  ... CN
R1 V11  V12 ... V1n
R2 V21  V22 ... V2n
.. ..   ..  ... ..
.. ..   ..  ... ..
Rn Vn1  ..  ... Vnn

Choose K rows from the table, sum up value on each column, result to {S1, S2,..., Sn} values.

If result {S1, S2,..., Sn} >= {P1, P2,..., Pn} at all elements, then we call K is valid combination.

Question: Minimize K.
Expect: Find approximation value of optimized K.


## Solution

- Find approximated value of optimized K.

	```js
	// When K is small (<= 10)
	// Have 2^K (<= 1024) combinations.
	// Just brute-force loop all combinations and find the best one.
	// TechNote: combination can be presented as binary at most K bits.

	// When K is large (> 10)
	// By repeating find the next best matched combination,
	// we can find combination set that conduces to solution.
	```
