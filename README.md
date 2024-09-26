## Dataset

This dataset, Tobacco_Inv_8.28.24_9.11.24.csv, was obtained from the Vendor Detail Report via LMS-POS from Bizi Mart in Antioch, CA.

This dataset contains information such as the count of tobacco items sold during a period of time (8/28/24 to 9/11/24) and the inventory count of the items.

## Python Code

- [View Bizi Mart Tobacco Reorder Point List (Version 1) ](https://kvellian.github.io/bizi_reorder_tobacco/assets/path/bizi_tobacco_reorder_v1.html)

## Purpose

This project aims to create a color-coded tobacco product shopping list for Bizi Mart that highlights levels of urgency to reorder (Red, Yellow, Orange, Green).

This project assigns box/case values to each product based on its type and calculates reorder points with this information.


## Use Case

Bizi Mart places bi-weekly orders for tobacco products with our vendor, PITCO FOODS. 


## Reorder Point Rules

Summary:

Red: Critical reorder needed - if Sold > On Hand or On Hand < Box.

Yellow: Moderate reorder point - if On Hand <= 1.5 * Sold or On Hand <= 1.5 * Box but greater than Box.

Orange: Approaching reorder point - if On Hand <= 2 * Sold but greater than 1.5 * Sold or On Hand <= 2 * Box but greater than 1.5 * Box.

Green: Sufficient stock - if On Hand > 2 * Sold and On Hand > 2 * Box.


## Output Result

https://kvellian.github.io/bizi_reorder_tobacco/assets/path/Bizi_Tobacco_List_9.11.24.htm
