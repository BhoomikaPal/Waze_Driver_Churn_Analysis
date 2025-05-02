# Waze User Churn Analysis

## Project Title
**Understanding driving behavior and churn patterns among Waze users**

## Project Overview
The goal of this project was to inspect and understand Waze's user driving data to explore user retention patterns and churn behavior.

Using a Pandas dataframe, summary statistics were compiled to compare users who churned versus those who were retained. Key insights were drawn regarding driving habits and potential user profiles. Initial exploration showed that churned users had different driving behaviors compared to retained users. The final deliverable informed next steps for further exploration and potential recommendations to Waze.

---

## Business Understanding
Waze users rely heavily on the app for navigation and trip planning.  
Understanding which users churn and why they churn is critical to improving the product and retaining users.  

By analyzing driver activity data (such as number of drives, driving days, kilometers driven, and device type), Waze can better identify patterns that predict churn and develop strategies to reduce it.  
This could ultimately improve user engagement and satisfaction with the app.

---

## Data Understanding
The data used in this project was a CSV file containing 14,999 rows and 13 columns, representing individual users and their recent driving activity metrics.

### Key Aspects:
- **Data Types**: float, int, and object.
- **Missing Labels**: 700 rows missing a churn label, appearing random without strong patterns.
- **Device Distribution**: ~36% Android users, ~64% iPhone users.
- **Churn Distribution**: No significant imbalance between device types.
- **Bias**: No strong signs of biased sampling, though additional verification suggested.

### Feature Engineering:
- Median values were preferred over means to handle outliers.
- Key behavioral metrics were engineered:
  - **Drives per Day**
  - **Kilometers per Drive**

---

## Modeling and Evaluation
No machine learning model was built at this stage.  
Instead, extensive **Exploratory Data Analysis (EDA)** was performed.

### Key Findings:
- **Driving Behavior**:
  - Churned users had more drives but fewer driving days.
  - Churned users drove longer distances and spent more time driving in the last month.
  - Per drive day, churned users drove significantly farther (~608 km/day), about **250%** higher than retained users.
- **Device Type**:
  - iPhone vs Android had **no significant effect** on churn likelihood.

**Insight**:  
There seems to be a "super-driver" profile — users who drive exceptionally long distances, possibly professional drivers (e.g., truckers), whose needs Waze might not currently fully meet.

---

## Conclusion
The investigation successfully identified important behavioral differences between users who churned and those who stayed.

**Most Distinguishing Features**:
- Number of drives
- Distance driven
- Time spent driving

Device type was **not** a major factor.

---

## Recommendations
- Conduct further qualitative research on "super-drivers" to better understand their needs.
- Develop targeted features or services for users who drive unusually long distances.
- Explore machine learning models to predict churn likelihood based on driving behaviors.
- Investigate user segmentation based on natural driving profiles.

**Note**:  
The missing labels did not appear to significantly bias the results.

---
