Waze-Driver-Data-Project
Project Title
Understanding driving behavior and churn patterns among Waze users.

Project Overview
The goal of this project was to inspect and understand Waze's user driving data to explore user retention patterns and churn behavior.
Using a Pandas dataframe, summary statistics were compiled to compare users who churned versus those who were retained. Key insights were drawn regarding driving habits and potential user profiles. Initial exploration showed that churned users had different driving behaviors compared to retained users. The final deliverable informed next steps for further exploration and potential recommendations to Waze.

Business Understanding
Waze users rely heavily on the app for navigation and trip planning.
Understanding which users churn and why they churn is critical to improving the product and retaining users. By analyzing driver activity data (such as number of drives, driving days, kilometers driven, and device type), Waze can better identify patterns that predict churn and develop strategies to reduce it. This could ultimately improve user engagement and satisfaction with the app.

Data Understanding
The data used in this project was a CSV file provided for analysis purposes. It contained 14,999 rows and 13 columns, representing individual users and their recent driving activity metrics.
Key aspects of the dataset:

Data types included float, int, and object.

700 rows (out of 14,999) were missing a label value, which identifies whether a user churned or was retained.

Missing values appeared random with no strong pattern tied to a specific device or driving behavior.

Device distribution was consistent across the dataset: approximately 36% Android users and 64% iPhone users.

There were no significant imbalances between devices regarding churn rates.

No strong signs of biased sampling were detected, but additional verification was suggested.

Feature engineering steps:

Median values were primarily used over means to account for outliers.

Key behavioral metrics such as drives per day and kilometers per drive were calculated to better understand user behavior.

Modeling and Evaluation
Although no machine learning model was constructed at this stage, extensive exploratory data analysis (EDA) was performed.

Key findings:

Churned users had more drives but fewer driving days compared to retained users.

Churned users drove longer distances and spent more time driving in the last month.

Per drive day, churned users drove significantly farther (~608 km/day) compared to retained users (~250% higher).

Device type (iPhone vs Android) did not significantly influence churn likelihood.

These behavioral patterns suggest the existence of a "super-driver" profile — users who may be professional drivers (e.g., long-haul truckers) whose needs Waze may not fully meet.

Conclusion
The data investigation successfully identified important behavioral differences between users who churned and those who stayed.
The most distinguishing features between churned and retained users were related to the number of drives, distance driven, and time spent driving rather than device type.

Recommendations for next steps:

Further qualitative research on high-activity users ("super-drivers") to understand their needs.

Potential targeted features or services for users who drive unusually long distances.

Explore machine learning models to predict churn likelihood based on driving behaviors.

Investigate natural segmentation of users based on their driving profiles.

The missing labels did not seem to bias the results significantly, and overall, the dataset provided strong initial insights into user retention patterns.

