# Amazon_Vine_Analysis

## Overview of the analysis: 
Reviews have been an important part of the consumer experience since the beginning of consumerism. If something does not have a good reputation, why waste time? Companies have found reviews so important to their success, they have resulted in incentivizing cosumers to review their products. This project was done to find a bias towards reviews done by the paid Amazon Vine program. Amazon Vine program allows manufacturers and publishers to get guaranteed reviews by paying a fee to Amazon and providing products to the members of the program. 

This project used data from Amazon reviews on pet products. Using PySpark, the ETL process was performed on the pet product dataset. The dataset was then connected to an AWS RDS instance and loaded into pgAdmin. The reviews were anazlyed using Pandas to find a bias in reviews. 

## Results: 
* How many Vine reviews and non-Vine reviews were there?
    * From the crude data: there were 10,215 Vine reviews and 2,633,399 non-Vine reviews.
    * From the "more than 50% helpful votes" category: there were 170 Vine reviews and 37,840 non-Vine reviews.
![yes_vine_df](https://user-images.githubusercontent.com/98570777/183361583-e823defd-d76d-4555-b38c-41fd975eb0d4.jpg)
![no_vine_df](https://user-images.githubusercontent.com/98570777/183361554-fc6f8736-9855-44c0-801b-54da5d7e9686.jpg)

* How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
    * From the "more than 50% helpful votes" and "5-star review" category: there were 65 Vine reviews and 20,612 non-Vine reviews.
![5_star_yes_vine_df](https://user-images.githubusercontent.com/98570777/183361409-cf1a954e-440a-4a1d-ac26-8ec42933e613.jpg)
![5_star_no_vine_df](https://user-images.githubusercontent.com/98570777/183361353-b1d2e8fd-7de9-440f-bbb1-0b0197265a88.jpg)

* What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
    * 0.31% of the helpful five star reviews on pet products are part of the paid Vine program.
    * 99.69% of the helpful five star reviews on pet products are not part of the Vine program.
![percentages](https://user-images.githubusercontent.com/98570777/183361723-ce210255-467b-4789-89bf-d6e83422120c.jpg)

## Summary: 
Based on the low percentage of 0.31% of significant reviews being from people that are part of the paid Vine program, it is not significant. 99.69% of the reviews that were rated as helpful and five-star were from people who genuinely enjoyed the products for their pets.

An additional analysis on each of the other helpful-rated, multi-star reviews can be done to see which ones were a part of the Vine program. The assumption in the above analysis was the Vine program participants would review the product well because they were paid. Doing an analysis on the lower star reviews could reveal that the Vine program could be hurting ratings.
