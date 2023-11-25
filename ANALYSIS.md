## Key Observations from Correlation Matrix Heatmap

The heatmap provides a visual representation of the correlation between different variables in the bank dataset. Below are the most significant observations:

- **Positive Correlations**:
  - `duration` shows a substantial positive correlation with the outcome variable `y`, indicating that longer last contact durations are strongly associated with a higher likelihood of a term deposit subscription.
  - `pdays` and `previous` exhibit a strong negative correlation with `campaign`, suggesting that a higher number of contacts in the current campaign is related to fewer contacts and a longer time since the last campaign.

- **Moderate Correlations**:
  - `housing` and `loan` display a moderate positive correlation, implying that clients with housing loans may also be more likely to have personal loans.
  - The `month` of contact shows a moderate positive correlation with `day`, which could indicate seasonal or monthly patterns in the contact strategy.

- **Negative Correlations**:
  - `pdays` (days since the last contact from a previous campaign) and `poutcome` (outcome of the previous marketing campaign) are negatively correlated with the outcome `y`, suggesting certain outcomes or longer periods since the last contact may decrease the likelihood of a term deposit subscription.

These insights are critical for understanding client behavior and can guide data-driven decision-making in campaign strategies.

![CorrMatrix](https://github.com/HrMav/Bank-Deposit-Machine-Learning-R/assets/132946730/0c5b7ef9-bca8-4049-b044-9260e61a8f51)


## Information Value Analysis Summary

### Highly Predictive Variables:
- **Duration (IV = 1.1353):** Extremely strong predictive power. This suggests that the last contact duration is a key factor in predicting the outcome.
- **Balance (IV = 0.7053):** Also very strong in predictive power, indicating that the average yearly balance is significantly influential.

### Moderately Predictive Variables:
- **Month (IV = 0.4361):** Moderate predictive power, showing the month of last contact has a notable influence.
- **Poutcome (IV = 0.5146):** The outcome of the previous marketing campaign is a moderately strong predictor.
- **Pdays (IV = 0.4949):** Days since the last contact from a previous campaign have a moderate influence.

### Variables with Medium Predictive Power:
- **Age (IV = 0.2231):** Fairly good predictive power, suggesting age has a reasonable influence.
- **Job (IV = 0.1557)** and **Housing (IV = 0.1887):** These have medium predictive power.
- **Previous (IV = 0.2290):** Number of contacts before this campaign has a similar influence as age.

### Variables with Low Predictive Power:
- **Education (IV = 0.0501), Loan (IV = 0.0549), Marital (IV = 0.0401), Campaign (IV = 0.0800):** These show low predictive power, suggesting they have limited influence on the outcome.
- **Day (IV = 0.1178):** Slightly higher but still low in terms of influencing the outcome.

### Least Predictive Variable:
- **Default (IV = 0.0063):** Very low predictive power, indicating this variable is not a significant factor in predicting the outcome.

### Overall Interpretation:
- The most crucial variables for predicting whether someone will subscribe to a term deposit appear to be the **duration** of the last contact and the client's **balance**.
- Variables related to the timing and outcome of previous contacts (**month**, **poutcome**, **pdays**) also hold moderate predictive power.
- Demographic factors like **age**, **job**, and **education**, while somewhat informative, are less impactful compared to contact-related variables.
- Variables like **default** have minimal influence and might not be useful in predictive modeling for this specific outcome.

## Cluster Analysis Results Interpretation

The cluster analysis of the bank dataset has revealed three distinct segments of clients based on various attributes:

### Cluster 1 Characteristics
- **Average Age**: 40.9 years old.
- **Job**: Diverse occupations with an average encoded value of 5.35.
- **Marital Status**: Majority in a similar marital status (encoded value: 2.16).
- **Education Level**: Average level of education (encoded value: 2.21).
- **Credit Default**: Very few clients with credit in default.
- **Average Balance**: €1049.
- **Housing Loan**: Approximately 53.6% have housing loans.
- **Personal Loan**: A smaller segment with personal loans.
- **Contact**: Primarily through one contact method (encoded value: 1.76).
- **Contact Day**: Most contacts around the 16th of the month.
- **Contact Month**: A mix throughout the year (encoded value: 6.46).
- **Duration**: Average last contact duration of 183 seconds.
- **Campaign Contacts**: Around 3 contacts per campaign.
- **Previous Campaign Contacts**: Very few previous contacts.
- **Outcome of Previous Campaign**: Generally unknown (encoded value: 3.98).
- **Term Deposit Subscription**: Low subscription rate (5.62%).

### Cluster 2 Characteristics
- **Average Age**: Similar to Cluster 1, around 40.8 years old.
- **Job**: Similar job distribution to Cluster 1.
- **Marital and Education**: Comparable marital status and education level to Cluster 1.
- **Credit Default**: Even fewer defaults than Cluster 1.
- **Average Balance**: Higher at €1479.
- **Housing and Personal Loans**: More clients with housing loans and slightly fewer with personal loans than Cluster 1.
- **Contact Method**: Slightly more varied than Cluster 1.
- **Contact Day and Month**: Similar pattern as Cluster 1 for contact days and months.
- **Duration**: Longer last contact duration averaging 243 seconds.
- **Campaign Contacts**: Fewer than Cluster 1.
- **Previous Campaign Contacts**: Significantly higher, indicating more follow-up was done with these clients.
- **Outcome of Previous Campaign**: Better outcomes (encoded value: 1.47).
- **Term Deposit Subscription**: Higher subscription rate (19.7%).

### Cluster 3 Characteristics
- **Average Age**: Slightly older than the first two clusters at 41.3 years.
- **Job and Education**: Job types and education levels are in line with the other two clusters.
- **Credit Default**: Low occurrence of defaults, slightly above Cluster 1.
- **Average Balance**: Significantly higher at €3279, indicating a wealthier segment.
- **Housing and Personal Loans**: Similar to Cluster 1 in terms of loans.
- **Contact Method**: Less variety in contact method compared to the other clusters.
- **Contact Day and Month**: Consistent with the other clusters.
- **Duration**: The longest average duration of 782 seconds.
- **Campaign Contacts**: Similar to Cluster 1.
- **Previous Campaign Contacts**: Lowest previous campaign contacts amongst the clusters.
- **Outcome of Previous Campaign**: Mostly unknown, akin to Cluster 1 (encoded value: 3.92).
- **Term Deposit Subscription**: Highest subscription rate (40.1%).

### Inferences
- **Cluster 2** represents a middle ground between the other two clusters, with slightly wealthier clients and a moderate subscription rate.
- **Cluster 3** clients, with the highest average balance and longest call duration, are the most likely to subscribe to term deposits, indicating the potential value in targeting similar profiles.
- **Cluster 1** has the lowest subscription rate, suggesting these clients may need a different approach or offer to be converted.

These clusters can provide actionable insights for targeted marketing campaigns, with tailored strategies for each segment to improve term deposit subscription rates.

