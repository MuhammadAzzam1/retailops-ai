# Sales Data Contract

## What one row represents
One row represents one product line in a sale. If a receipt contains three different products, the sales file has three rows for that receipt.

## How to identify one row
The combination of sale_id and line_number identifies a row. sale_id alone can repeat because one sale can contain multiple products.

## Fields needed
sale_id — receipt or sale identifier
line_number — line number within that sale
sale_date — date of the sale
outlet_id — outlet where the sale happened
sku — product identifier
quantity — number of units sold
unit_price_pkr — price per unit at the time of sale