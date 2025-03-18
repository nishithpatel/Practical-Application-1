Below is a summary of findings from our analysis on whether a customer will accept a coupon or not.  Details can be found in this [jupyter notebook](https://github.com/nishithpatel/Practical-Application-1/blob/main/Analyze%20if%20the%20Customer%20Accept%20the%20Coupon.ipynb). 

## Data Quality
* Missing values are limited to columns: car, Bar, CoffeeHouse, CarryAway, RestaurantLessThan20 and Restaurant20To50
* Missing values for column car: 99% (12,576).  This means that car column is not useful and can be excluded from our analysis.
* 12079 rows i.e. 95% rows remain even after we drop rows with missing values in one of the following columns: Bar, CoffeeHouse, CarryAway, RestaurantLessThan20 and Restaurant20To50
* Column 'age' has the following values: below21, 21, 26, 31, 36, 41, 46, 50plus  which can be confusing unless you have the context that they represent ranges. These values were updated to: 20 and below, 21 to 25, 26 to 30, 31 to 35, 36 to 40, 41 to 45, 46 to 50 and 51 and above.
* Column name 'passanger' was updated to 'passenger'

## Overall findings 
* 56.93% coupons were accepted
* "Carry Out and Take away" coupon had the highest acceptance rate of 73.77% followed by "Restaurant<20" coupon with 70.9% acceptance rate

### Bar Coupon
* "Bar" coupon had the least acceptance rate of 41.19%
* Acceptance Rate for drivers who go to a bar more than once a month is similar irrespective of the age.
* Acceptance Rate for drivers who go to a bar more than once is more than double of those who go to a bar at most once a month.

### Carry Out and Take Away
* Carry out & Take away coupon has the highest acceptance rate of 73.77%.
* Based on analyzing data for this coupon type combined with destination, direction of driving, time to drive to venue: 
  * Destination "Home" and "No Urgent Place" have a much higher acceptance rate compared to "Work" (at least 10% more)
  * Venue Direction, Time to Drive to Venue >= 15 minutes and Time to Drive to Venue >= 25 minutes do not have a significant impact on overall coupon acceptance rate independently.
  * Coupon Acceptance Rate for "No Urgent Place" as destination is 0% if a. Venue Direction is the same as the Destination or b. Time to Drive to Venue is more than 25 minutes
