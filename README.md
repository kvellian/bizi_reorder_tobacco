## Dataset

This dataset, Tobacco_Inv_8.28.24_9.11.24.csv, was obtained from the Vendor Detail Report via LMS-POS from Bizi Mart in Antioch, CA.

This dataset contains information such as the count of sold tobacco items during a period of time (8/28/24 to 9/11/24 in this experiment) and the inventory count of the items.

I manually assigned the vendor (PITCO FOODS) to over 270 tobacco products in our system to ensure they will be included in this report, when applicable.

## Python Code

- [View Bizi Mart Tobacco Reorder Point List (Version 1) ](https://kvellian.github.io/bizi_reorder_tobacco/assets/path/bizi_tobacco_reorder_v1.html)

## Purpose

This project aims to create a color-coded tobacco product shopping list for Bizi Mart that highlights levels of urgency to reorder (Red, Yellow, Orange, Green).

This program assigns box/case values to each product based on its brand and type and calculates reorder points using this information.

NOTE: This program is still a work in progress. Some items have not been assigned case/box values and may not have color-coding in the final result. 
However, in the meantime, the reader can still evaluate the units sold and units on hand columns before placing an order.

Eventually, I will make a color-coded list, similar in concept, for our liquor products.

Please see the current output/results below.


## Use Case

Bizi Mart places biweekly orders for tobacco products with our vendor, PITCO FOODS. Previously, the shopping list was handwritten or typed. Occasionally, products that were empty on shelves would be forgotten when ordering. 

The operations manager will create a CSV of the Vendor Detail Report for tobacco products sold over a 2-week period via LMS-POS. Afterward, the report will be run through the program to generate a color-coded list via Excel. This list will be used to make more informed decisions when ordering tobacco products.

## Reorder Point Rules

**Summary**:

<span style="background-color: red; color: white; padding: 2px;">Red (Critical):</span> Critical reorder needed - if Sold > On Hand or On Hand < Box.
- If we sold more units than we currently have in stock or if we have less than a case/box in stock.
- Reorder products immediately.
  
<span style="background-color: yellow; color: black; padding: 2px;">Yellow (Moderate):</span> Moderate reorder point - if On Hand <= 1.5 * Sold or On Hand <= 1.5 * Box but greater than Box.
- If inventory is less than or equal to 1.5 times the number of units sold. Or if inventory is less than or equal to 1.5 times a case/box.
- Stock levels are getting low, order a few cases/boxes to cover 2 weeks.

<span style="background-color: orange; color: white; padding: 2px;">Orange (Approaching): </span> Approaching reorder point - if On Hand <= 2 * Sold but greater than 1.5 * Sold or On Hand <= 2 * Box but greater than 1.5 * Box.
- If inventory is less than or equal to 2 times the number of units sold but greater than 1.5 times the units sold. Or if inventory is less than or equal to 2 times the case/box by greater than 1.5 times the units sold.
- Monitor the product trend. Potentially reorder in 2 weeks.

<span style="background-color: green; color: white; padding: 2px;">Green (Sufficient): </span> Sufficient stock - if On Hand > 2 * Sold and On Hand > 2 * Box.
- If inventory is greater than 2 times the number of units sold and inventory is greater than 2 times case/box.
- No need to reorder this period.




## Output Result - Excel File

- [Bizi Mart Tobacco Reorder Point List](https://kvellian.github.io/bizi_reorder_tobacco/assets/path/Bizi_Tobacco_List_9.11.24.htm)

## Tobacco List

<iframe src="https://kvellian.github.io/bizi_reorder_tobacco/assets/path/Bizi_Tobacco_List_9.11.24.htm" 
        width="100%" 
        height="600px" 
        frameborder="0">
</iframe>


