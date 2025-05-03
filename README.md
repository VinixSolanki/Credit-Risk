#   Credit Risk Analysis - A Business Case for New Market Entry

##  Overview

This Power BI project provides a comprehensive analysis of credit risk to inform strategic decisions regarding new market entry. The dashboard incorporates various visualizations and a custom risk scoring model to assess borrower profiles and identify potential opportunities and challenges in different regions.

Key security measures, specifically Row-Level Security (RLS), have been implemented to ensure data privacy and compliance. RLS restricts data access based on user roles (region or department), allowing users to view only the data relevant to their responsibilities. [cite: 1, 2, 3]

##  Key Features

* **Interactive Dashboard:** Provides a visual exploration of loan data, risk scores, and geographical distribution.
* **Custom Risk Scoring Model:** Utilizes a DAX formula incorporating loan amount, borrower's income percentage, employment length, and default history to assess credit risk. [cite: 56]
* **Row-Level Security (RLS):** Ensures data privacy by restricting data access based on user roles (region or department). [cite: 1, 2, 3]
* **Geographical Analysis:** A bubble map visualization highlights loan activity and potential in different regions. [cite: 45, 46, 47]
* **Time Series Analysis:** Tracks risk scores across different loan intents over time.

##  Security Features

This project implements Row-Level Security (RLS) to protect sensitive data.

* **Mechanism:** Data access is restricted based on the user's region or department. [cite: 1, 2, 3]
* **Implementation:**
    1.  A `Security` table links usernames to their corresponding region or department. [cite: 3]
    2.  A relationship is established between the `Security` table and the main data table using the Region or Department fields. [cite: 3]
    3.  DAX expressions within Power BI roles (`[Region] = LOOKUPVALUE(Security[Region], Security[Username], USERNAME())`) enforce the row-level filtering. [cite: 3]
    4.  Testing is conducted using the "View as Roles" feature in Power BI Desktop before publishing to the Power BI Service. [cite: 3]
    5.  Users are assigned to specific roles within the Power BI Service. [cite: 3]

##  Key Observations from the Analysis

* **Risk Score Insights:**
    * Higher risk scores are often associated with loan intents focused on long-term returns (e.g., education, venture), potentially due to delayed repayment. [cite: 3, 60]
    * Education loans currently exhibit the highest risk score (52K). [cite: 57]
    * Including employment length and default history significantly improves the identification of unstable borrower profiles. [cite: 4, 61]
    * Home Improvement loans show the lowest risk scores, suggesting greater stability. [cite: 59]
* **Geographical Insights:**
    * Loan activity is concentrated in developed regions, indicating a correlation between lending and economic infrastructure. [cite: 52]
    * Africa and Antarctica appear to have no recorded loan data in this view. [cite: 51]
    * The absence of data in certain areas might represent untapped markets or limited access to lending systems. [cite: 53]
    * Bubble maps are valuable for identifying high-performing regions and exploring underserved markets for potential expansion. [cite: 54]
* **Loan Grade Analysis:**
    * Loan grades A to C tend to have lower average loan amounts and lower interest rates, resulting in lower default rates. [cite: 11]
    * Loan grades D to G show an increasing trend in both interest rates and default rates, indicating higher borrower risk. [cite: 12]
    * A clear correlation is seen between higher interest rates and default likelihood. [cite: 13]
* **Loan Status and Home Ownership:**
    * A large portion of borrowers (78.18%) did not default, while 21.82% did. [cite: 15]
    * Borrowers with mortgages and longer employment length show a tendency towards lower defaults. [cite: 16]
    * Renters show a higher concentration of defaults, highlighting potential financial instability. [cite: 16]
* **Credit History Impact:**
    * Default rates remain fairly stable for credit history lengths between 2 to 18 years. [cite: 27]
    * A noticeable increase in default rates starts after 20 years of credit history. [cite: 28]
* **Interest Rate Impact:**
    * There is a clear positive correlation between interest rates and default rates. [cite: 36, 37]
    * A significant increase in defaults is observed once the interest rate crosses 20%. [cite: 39]

##  Visualizations Included

* **Dashboard:** A comprehensive view displaying key metrics such as average loan to income ratio, average loan amount per grade, adjusted default rate by interest rate simulation, segmentation analysis using loan intent, financial metrics, risk score by loan intent, and loan status. [cite: 6, 7]
* **Bubble Map:** A geographical representation of total loan amounts across various global regions, with bubble size indicating loan volume. [cite: 45, 46, 47]
* **Time Series Analysis (Risk Score by Loan Intent):** A chart showing the fluctuation of risk scores across different loan intents, highlighting variations in risk associated with each loan category. [cite: 55, 56, 57]
* **Financial Metrics by Loan Grade:** Analysis presenting key financial metrics segmented by loan grade, providing insights into lending risk and borrower behavior. [cite: 10, 11, 12, 13, 14, 15]
* **Loan Status Distribution:** Visualization of loan status (default or non-default) and its relation to employment length and home ownership. [cite: 15, 16, 17]
* **Segmentation Analysis Using Loan Intent:** Compares average loan amount, average interest rate, and default rate across different loan grades. [cite: 17, 18, 19, 20, 21, 22, 23, 24]
* **Time Series Analysis (Default Rate by Credit History Length):** Examines how loan default rates vary with the length of a borrower's credit history. [cite: 25, 26, 27]
* **Impact of Interest Rate on Default Rate:** Simulation exploring the potential impact of varying interest rates on loan default rates. [cite: 34, 35, 36, 37]

##  Conclusion and Recommendations

The insights from this credit risk analysis provide valuable information for strategic decision-making regarding new market entry. The risk scoring model and geographical analysis help identify both high-potential and high-risk areas. The implementation of RLS ensures data security and compliance.

Further investigation into underserved markets and a deeper analysis of the factors contributing to higher risk scores for specific loan intents could provide even more actionable insights.



##  Thank You
