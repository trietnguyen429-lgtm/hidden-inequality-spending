Hidden Inequality in Everyday Spending
A SQL Analysis of CFPB Consumer Complaint Data
By Triet Minh Nguyen

Overview
This project uses SQL to analyze over 3 million consumer complaints filed with the Consumer Financial Protection Bureau (CFPB). The goal is to uncover patterns of inequality in how financial products are complained about, and how companies respond or fail to respond to the most vulnerable consumers.

Key Question: Are consumers of high-risk financial products like payday loans and debt collection services being systematically underserved compared to others?
Spoiler: Yes.

Source: Google BigQuery Public Datasets
Table: bigquery-public-data.cfpb_complaints.complaint_database
Size: 3+ million complaints
Columns include: product, issue, company name, state, company response, timely response, date received

Findings
1. Credit Reporting Dominates Complaints
Credit reporting alone accounts for over 1.7 million complaints — nearly 4x more than debt collection in second place. The big three credit bureaus (Equifax, TransUnion, Experian) are responsible for over 1.6 million complaints combined, more than all major banks combined.
2. Certain States Are Disproportionately Affected
California, Florida, and Texas lead in total complaints as expected by population. However, Georgia punches significantly above its weight, ranking 5th nationally despite being the 8th most populous state.
3. Companies Rarely Deliver Real Relief
Of all complaints resolved:

- 2.6 million were closed with just an explanation
- Only 129,000 received actual monetary relief — less than 4% of all complaints
- 9,489 received untimely responses, meaning companies missed deadlines entirely

4. Vulnerable Products Get the Slowest Responses
Payday loans have a 10.77% untimely response rate — the second highest of any product category. These are products used primarily by low-income consumers who are least able to wait for resolution.
5. Debt Collection Consumers Get the Least Relief
Of 473,000 debt collection complaints, only 4,082 resulted in monetary relief — less than 1%. The vast majority were closed with an explanation and nothing more.

Queries:
query1_complaints_by_product.csv = Total complaints by financial product
query2_complaints_by_state.csv = Total complaints by state
query3_complaints_by_company.csv = Top 10 most complained about companies
query4_company_responses.csv = Breakdown of how companies respond to complaints
query5_untimely_by_product.csv = Untimely response rates by product category
query6_vulnerable_product_responses.csv = Response breakdown for payday loans, debt collection, and mortgages

Tools Used

SQL (Google BigQuery)
Google BigQuery Public Datasets
GitHub


Conclusion
The data tells a clear story: the financial products most used by vulnerable, low-income consumers generate the most complaints, receive the slowest responses, and deliver the least meaningful relief. The system exists, but it is not working equally for everyone.
