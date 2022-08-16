**Project Title**

Driving Customer Coupon Analysis

Link to Jupyter notebook below:

https://github.com/philipMLdatascientist/Amazon-Driving-Customer-Coupon-Analysis/blob/main/Customer%20Coupon%20Analysis.ipynb

**Project Description.**

Will a Customer Accept the Coupon?


**Context**

Imagine driving through town and a coupon is delivered to your cell phone for a restaraunt near where you are driving. Would you accept that coupon and take a short detour to the restaraunt? Would you accept the coupon but use it on a sunbsequent trip? Would you ignore the coupon entirely? What if the coupon was for a bar instead of a restaraunt? What about a coffee house? Would you accept a bar coupon with a minor passenger in the car? What about if it was just you and your partner in the car? Would weather impact the rate of acceptance? What about the time of day?

Obviously, proximity to the business is a factor on whether the coupon is delivered to the driver or not, but what are the factors that determine whether a driver accepts the coupon once it is delivered to them? How would you determine whether a driver is likely to accept a coupon?

**Overview**

The goal of this project is to use what you know about visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those that did not.

**Data**

This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios including the destination, current time, weather, passenger, etc., and then ask the person whether he will accept the coupon if he is the driver. Answers that the user will drive there ‘right away’ or ‘later before the coupon expires’ are labeled as ‘Y = 1’ and answers ‘no, I do not want the coupon’ are labeled as ‘Y = 0’.  There are five different types of coupons -- less expensive restaurants (under \\$20), coffee houses, carry out & take away, bar, and more expensive restaurants (\\$20 - \\$50). 

**Deliverables**

A brief report that highlights the differences between customers who did and did not accept the coupons.  An exploratory data analysis will be performed using knowledge of plotting, statistical summaries, and visualization using Python.

**Data Description**

The attributes of this data set include:
User attributes
Gender: male, female
Age: below 21, 21 to 25, 26 to 30, etc.
Marital Status: single, married partner, unmarried partner, or widowed
Number of children: 0, 1, or more than 1
Education: high school, bachelors degree, associates degree, or graduate degree
Occupation: architecture & engineering, business & financial, etc.
Annual income: less than $12500, $12500 - $24999, $25000 - $37499, etc.
Number of times that he/she goes to a bar: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
Number of times that he/she buys takeaway food: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
Number of times that he/she goes to a coffee house: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
Number of times that he/she eats at a restaurant with average expense less than $20 per person: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
Number of times that he/she goes to a bar: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
Contextual attributes
Driving destination: home, work, or no urgent destination
Location of user, coupon and destination: we provide a map to show the geographical location of the user, destination, and the venue, and we mark the distance between each two places with time of driving. The user can see whether the venue is in the same direction as the destination.
Weather: sunny, rainy, or snowy
Temperature: 30F, 55F, or 80F
Time: 10AM, 2PM, or 6PM
Passenger: alone, partner, kid(s), or friend(s)
Coupon attributes
time before it expires: 2 hours or one day

**Summary of Findings**

Bar Coupon Analysis

The overall proportion of bar coupons that drivers chose to accept is 41.2%. This approximates the acceptance rate of drivers who go to restauratns that cost less than $20 more than 4 times a month and whose income is less than 50k. However, the acceptance rate for drivers who go to a bar more than once a month and are over the age of 25 is 69 percent; the acceptance rate for drivers who go to a bar 3 or more times a month is 76.2 percent; the acceptance rate of drivers who go to bars more than once a month, had passengers that were not a kid, and had occupations other than farming, fishing, or forestry is 70.9 percent; the acceptance rate between drivers who go to bars more than once a month, had passengers that were not a kid, and were not widowed is 70.9 percent; the acceptance rate of drivers who go to bars more than once a month and are under the age of 30 is 72.0 percent. The data supports the hypothesis that past behavior of frequenting a bar more than once a month has a strong predictive effect on whether the driver will accept to use a bar coupon to the exclusion of all others features. Would past behavior concerning the other coupon categories have the same predictive affect on coupon acceptance rate? This hypothesis will need to be further tested to confirm its validity and generizability to future data samples.

Comparison of Feature Affect On Acceptance Rates between Restaurant <$20 and Restaurant $20-$50 coupons

Destination | No Urgernt Place & Home: The Restaurant(< 20) coupon accepetance count is nearly 4 times that of the no acceptance count in the "No Urgent Place" category. However, the Restaurant $20-50 coupon acceptance and no acceptance counts are nearly equivalent for the same category. Furthermore, the highest acceptance count for the Restaurant 20-50 coupon is in the "Home" category but the value is surpassed by the no acceptance count. The "Work" category no acceptance count is also markedly higher.

Recommendation: Restaurants < 20 should send their coupons outside of morning and afternoon rush hour. Restaurants 20-50 should send their coupons during afternoon rush hour.

Passenger | Alone & Friend: The Restaurant < 20 coupon acceptace count for 'Alone & Friend' are markedly higher than the no acceptance count. However, the Restaurant 20-50 coupon acceptance count is lower in both aformentioned categories but markedly so in the 'Friend' category. The highest acceptance count for both coupons is in the 'Alone' category.

Recommendation: Coupons for Restaurants < 20 & 20-50 should be sent during lunch breaks when people tend to eat by themselves. It is difficult to predict when a driver would have a friend in the car but perhaps Federal Holidays would also be another reasonable target for Restaraunt < 20 coupons.

Weather | Sunny: Both coupons have the highest acceptance count in the "Sunny" catgory and very low acceptance rates during snowy and rainy weather.

Recommendation: Only send coupons during sunny weather.

Temperature | 80F: Both coupons have their highest acceptance count during 80F, followed by 55F, followed by 30F. However, the effect is most pronounced at 80F.

Recommendation: Both coupons should be sent when temperatures approximate 80F but temperatures of 55F also produce reasonable acceptance counts.

Time | 7AM, 2PM, 6PM: Both coupons have their highest acceptance count at 6PM which reinforces previous findings. The Restaurant <20 coupon has its second highest acceptance count at 2PM and the Restaurant 20-50 coupon has its second hightest count at 7AM, which is still lower than the Restaurant less than 20 coupon at the same time.

Recommendation: Send the Restaurant <20 coupon at 7AM, 2PM, & 6PM. Send the Restaurant 20-50 coupon at 7AM and 6PM.

Expiration | 1d & 2h: Both coupons have higher acceptance counts with expirations lasting 1 day. However, the Restaurant <20 coupon also has a high acceptance count with an expiration of 2 hours.

Recommendation: Both expirations work well for the Restaurant <20 coupon. The Restaurant 20-50 coupon should have an expiration of 1 day.

Gender: Males and females demonstrate equivalent acceptance counts for either coupon. However, in this data set there are much higher acceptance counts for the Restaurant <20 coupon.

Recommendation: None.

Age | 21, 26, 31: Both coupons have the highest acceptance counts in the 21, 26, and 31 age categories. However, the Restaurant <20 has a higher acceptance vs no acceptance count across all age categories. The alternative coupon only had a higher acceptance rate in the 26 and 46 age categories.

Recommendation: The Restaurant <20 is effective for all age categories. The Restaurant <20-50 coupon does well for the 26 and 46 age categories and less so for the 21 and 31 age categories but can still generate significant reasonable counts.

Marital Status | Single, Married partner, Unmarried partner: Both coupons have the highest acceptance counts in the Single, Married, and Unmarried partner categories. However, the Restaurant less than $20 has a higher acceptance vs no acceptance count across all maritalStatus groups whereas these same findings are reversed for the Restaurant $20-50 coupon but still generates significiant acceptance counts.

Recommendation: The Restaurant <20 is effective for all marital status categories. The Restaurant 20-50 coupon does well for the single and married partner categories and less so for the unmarried partner category but can still generate significant acceptance counts.

Has_Children: Having children or not demonstrates similar acceptance rates for either coupon. However, in this data set there are much higher acceptance counts for the Restaurant <20 coupon.

Recommendation: Both coupons can drive acceptance counts by focusing on drivers who don't have children. The effect is more pronounced for the Restaurant <20 coupon.

Education | Bachelors & Some College - no degree: Both coupons had their highest acceptance counts for the bachelors and some college categories. However, the acceptance vs no acceptance rate for the Restaurant<20 is higher throughout all education categories. The acceptance rate for the Restaurant20-50 is only higher in the high school graduate and some high school categories.

Recommendation:Both coupons should be sent to drivers with a bachelor degree or some college education.

Income: The Restaurant < 20 coupon has a higher acceptance vs no acceptance rate accross all income categories. The Restaurant 20-50 coupon only has a higher acceptance vs no acceptance rate in the 25000-37499 and the 100000 or more categories. Interestingly, both coupons had their highest and second highest acceptance counts in the 25000-37499 and the more than 100000 category, respectively.

Recommendation: The Restaurant <20 coupon performs well across all income categories. The Restaurant 20-50 coupon has the highest acceptance rate among drivers who are in the 25000-37499 and the more than 100000 categories and still produces adequate acceptance counts in the 50000-62499 and 37500-49999 income categories.

Restaurant<20 | 1-3, 4-8: Both coupons have their highest acceptance counts within the 1-3 and 4-8 categories. However, the acceptance rate is significanty higher for the Restaurant<20 coupon in the 1-3 and 4-8 categories. This also supports my initial hypothesis that past behavior is strongly predictive of future coupon acceptance rate.

Recommendation: Send both coupons to drivers who frequent Restaurants<20 1-8 times a month.

Restaurant20-50 | less1, 1-3: Both coupons have their highest acceptance counts within the less1 and 1-3 categories. However, the acceptance rate is significanty higher for the Restaurant<20-50 coupon in the 1-3, 4-8, and gt8 categories. This also supports my initial hypothesis that past behavior is strongly predictive of future coupon acceptance rate.

Recommendation: Send both coupons to drivers who frequent Restaurants20-50 less1 and up to 3 times a month. Send Restaurant20-50 coupons to drivers who frequent Restaurant20-50 more than three times a month.

Occupation | Student, Unemployed, Computer & Mathematical, Sales & Related: Interestingly, the four occupation categories that had the highest counts in both coupons are the same - Student, Unemployed, Computer & Mathematical, Sales & Related. The acceptance vs no acceptance rate for the Restaurant <20 coupon is greater across all occupations with the exception of "building & grounds cleaning & maintenance" category.

In regards to the Restaurant 20-50 coupon, this is the first time the data set has shown me numerous categories that have acceptance rates higher than or equivalent to the no acceptance rates. These categories are specifically:

Healthcare Support, Healthcare Practioners & Technical, Sales & Related, Computer & Mathemmatical, Personal Care & Service, Office & Administrative Support, Construction & Extraction, Legal, and Production Occupations.

Recommendation: For the Restaurant <20 coupon focus on drivers who are students, unemployed, in the Computer & Mathematical or Sales & Related professions. For the Restaurant 20-50 focus on the same drivers as the other coupon and who work in the previously identified occupations above.
