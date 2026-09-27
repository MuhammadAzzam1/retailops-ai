# Interview Notes

## Data grain
- Meaning:Data grain defines what one row in a dataset represents. In RetailOps AI, one sales row represents one product line on a receipt. A receipt with three products produces three sales rows.
- RetailOps example: Sale S1001 contains Dalda and rice, so it produces two sales rows, one for each product line.

## Composite key
- Meaning:A composite key uses two or more columns together to uniquely identify a row. For sales lines, (sale_id, line_number) is the key. sale_id alone is insufficient because one sale can contain multiple product lines.

- Why sale_id alone is not enough:
Sale_id identifies the whole receipt, not each product on it.
If sale S1001 contains Dalda and rice, both rows have sale_id = S1001. So sale_id cannot tell us which row we mean. Adding line_number does:
- (S1001, 1) → Dalda
- (S1001, 2) → rice
That’s why sale_id + line_number identifies one specific sales row.

- RetailOps example: Sale S1001 has Dalda on line 1 and rice on line 2. (S1001, 1) and (S1001, 2) identify the two rows separately.
