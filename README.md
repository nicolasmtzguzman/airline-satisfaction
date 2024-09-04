# Airline Passenger Satisfaction
## Objective
Analyze airline passenger satisfaction data to uncover key insights and trends that influence overall customer satisfaction. Using Power BI, the data will be transformed into an interactive and visually compelling dashboard that provides a comprehensive view of factors affecting passenger experiences. Finally, explore several models of binary classification to predict whether a customer was satisfied or unsatisfied.
## Data Description
[Passenger Satisfaction Data](https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction)


**Gender**: Gender of the passengers (Female, Male)\
**Customer Type**: The customer type (Loyal customer, disloyal customer)\
**Age**: The actual age of the passengers\
**Type of Travel**: Purpose of the flight of the passengers (Personal Travel, Business Travel)\
**Class**: Travel class in the plane of the passengers (Business, Eco, Eco Plus)\
**Flight Distance**: The flight distance of this journey\
**Inflight Wifi Service**: Satisfaction level of the inflight wifi service (0:Not Applicable;1-5)\
**Departure/Arrival Time Convenient**: Satisfaction level of Departure/Arrival time convenient\
**Ease of Online Booking**: Satisfaction level of online booking\
**Gate Location**: Satisfaction level of gate location\
**Food and Drink**: Satisfaction level of food and drink\
**Online Boarding**: Satisfaction level of online boarding\
**Seat Comfort**: Satisfaction level of seat comfort\
**Inflight Entertainment**: Satisfaction level of inflight entertainment\
**On-Board Services**: Satisfaction level of on-board services\
**Leg Room Service**: Satisfaction level of leg room service\
**Baggage Handling**: Satisfaction level of baggage handling\
**Check-in Service**: Satisfaction level of check-in service\
**Inflight Service**: Satisfaction level of inflight service\
**Cleanliness**: Satisfaction level of cleanliness\
**Departure Delay in Minutes**: Minutes delayed when departure\
**Arrival Delay in Minutes**: Minutes delayed when Arrival\
**Satisfaction**: Airline satisfaction level(Satisfaction, neutral or dissatisfaction)
## Exploratory Data Analysis
Let's view the percentage distribution of all the categorical features:
![Screenshot 2024-09-03 154842](https://github.com/user-attachments/assets/d938be53-33b3-4b2a-b00f-95ad12610605)

**Sample Insights**
- There is roughly the same amount of men and women in the sample.
- The vast majority of the sample are loyal (repeat) passengers.
- Almost 70% of the passengers fly for business, rather than personal travel.
- Most passengers fly business or eco class, making up 93% of the sample.
- A majority of passengers were satisfied with several of the in-flight factors, like leg room and seat comfort.
- A majority of passengers were neutral or unsatisfied with factors like wifi and online booking.

Now, let's look at a few histograms:

![Screenshot 2024-09-03 164127](https://github.com/user-attachments/assets/312f1ee6-6edb-404a-b7f6-d4e9fe5010ec)![Screenshot 2024-09-03 164150](https://github.com/user-attachments/assets/39dbddf4-f14a-4f2f-a93a-0ff7ad62d741)
![Screenshot 2024-09-03 164206](https://github.com/user-attachments/assets/75b5dc2a-aea5-41a2-a02a-d52271add5ca)

From the plots we can conclude:
- Most of the passengers are ages 20-50.
- The loyal customers fly business class.
- Those who fly longer distances, fly in the business class

Finally, let's look at the count of satisfied vs unsatisfied passengers for each of the satisfaction level features:
![Screenshot 2024-09-03 165458](https://github.com/user-attachments/assets/f7f5179e-2e45-4f33-896d-57c3042309ef)
![Screenshot 2024-09-03 165531](https://github.com/user-attachments/assets/9def94a1-ad05-481a-a23f-71f78afd7413)

Some important insights:
- Almost all passengers who rated the wifi service a 5 were satisfied.
- The majority of passengers who rated ease of online booking and online check-in highly were satisfied.
- Features like departure/arrival time convenient and gate location had more unsatisfied passengers even when they were rated high.
## Binary Classification Models
Four different models were trained to predict whether a passenger would be satisfied or unsatisfied. The following are the results:
|                       | K-Nearest Neighbors | Random Forest | AdaBoost | Gradient Boosting |
|-----------------------|---------------------|---------------|----------|-------------------|
| Training Sample Error | 0.053               | 0.000         | 0.071    | 0.055             |
| Test Sample Error     | 0.064               | 0.040         | 0.070    | 0.057             |
| Accuracy              | 93.6%               | 96.0%         | 93.0%    | 94.3%             |

## Dashboard
- KPI's
  1. Total Passengers
  2. Average Total Rating
  3. Number of Satisfied Passengers
  4. Number of Unsatisfied Passengers
  5. Average Age
  6. Average Flight Distance
- Average Ratings for all In-Flight and Airline Services
- Satisfaction by Age Bar Chart
- Satisfaction by Class Column Chart
- Satisfaction by Loyalty Donut Chart
- Slicers
  1. Gender
  2. Customer Type
  3. Class
  4. Travel Type

![Screenshot 2024-09-03 173707](https://github.com/user-attachments/assets/f63c00ed-669a-4284-8945-f000ef25566c)
## Analysis
**1. Demographic Insights**
- Satisfaction does not appear to vary by gender. 44% of males were overall satisfied and 43% of females were overall satisfied.
- Satisfaction does not vary by age.
- 76% of disloyal passengers were unsatisfied, while a lower 52% of loyal passengers were unsatisfied. Therefore, disloyal passengers are more likely to be unsatisfied. Explore more to find out what factors lead to this.

**2. Travel Purpose and Class Insights**
  - Only 10% of passengers traveling for personal reasons were satisfied, while 59% of passengers traveling for business reasons were satisfied.
  - Satisfaction varies by class as 69% of passengers flying business class were satisfied, while only 18% of passengers flying eco class were satisfied.
  - Overall, this shows that services involving the economy class need to be improved.

**3. Service and Experience Evaluation**
- Inflight Wifi Service is strongly correlated with passenger satisfaction as almost all passengers who rated it a 5 were overall satisfied.
- Other strongly correlated features are online boarding and ease of online booking.
- Ground services like gate location and baggage handling aren't correlated with satisfaction as the majority of passengers who rated it highly were still unsatisfied



