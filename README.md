# Introduction

This is a python notebook where I analyse data from a client, Sprocket Central Pty Ltd, selling bicycles and accessories.
The aim is to recommend which customers to approach from a target dataset to market their products with high confidence of success.

## Data Quality Assessment

I analyse data for possible quality issues in the following areas:

* Accuracy - correctness of values
* Completeness - all data fields with values
* Consistency - no contradictions between values in same column, table
* Currency - values should be up to date
* Relevancy - data applicable to task at hand
* Validity - data contains allowable values
* Uniqueness - there should be no duplicates

## Missing Values

There were some columns which had related product information i.e. product_class, product_line e.t.c which were missing values in the same rows. Another column had a standard_cost which was positively correlated to a list_price column with full information. I leveraged this relation to fill in all missing values in these related columns using a K Nearest Neighbor algorithm from the Sci-Kit Learn library.

However, missing data in columns with demographic information like property_valuation and state were filled in using the mode of those columns.
