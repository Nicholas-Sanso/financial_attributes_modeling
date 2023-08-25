Catherine Sanso, Nicholas Sanso <br>
Aug 25, 2023 <br>
Project 4: <br>

# **Analyzing Financial Statement Line Items using Unsupervised Learning Techniques**


## Table of Contents:

1. [Background](#section-title)
1. [Problem Statement](#section-title) 
1. [Target Audience](#section-title)
1. [Research Approach](#section-title)
1. [Data Dictionary](#section-title)
1. [Discussion & Recommendations](#section-title)
1. [Software Required](#section-title)
1. [Sources](#section-title)
1. [Licensing](#section-title)


The remainder of this project is broken up across several self-containing notebooks containing indivdualized imports, code, and datasets. 
1. [Cleaning](#section-title)
1. [EDA](#section-title)
1. [Unsupervised Learning for Feature Extraction](#section-title) 
1. [Supervised Learning for Inference](#section-title)
1. [Evaluation, Conclusion, & Recommendations for Further Study](#section-title)

# [Background](#section-title)
Financial statements are documents that capture and communicate a business's acitvities and broadly fall into three categories: income statement, cash flows, and balance sheet.
- The income statement details the revenues a company has earned using the accrual principle, and mostly recognizes revenues earned for goods already shipped and services already provided. The income statement recognizes expenses incurred following the matching principle, and thus only recognizes expenses that can be traced to the revenues that were earned under the accrual principle. The income statement provides information on the revenue and cost structure of the firm, allowing the reader to infer the firm's profitability metrics.
- The cash flow statement details the movement of money into and out of the firm. The cash flow statement is broken down into three subcategories, operating cash flow, which captures the movement of cash related to standard business activities, investing cash flow, which captures the movemenet of cash related to the purchase or sale of capital assets, and financing cash flow, which captures the movement of cash between the firm and its investors/creditors.
- The balance sheet statement provides a snapshot of the firm at a single point of time. The balance sheet provides information on the liquidity (ability to meet short-term financial obligations), solvency (ability to meet long-term financial obligations), and leverage (amount of debt firm uses relative to its assets) of the firm. The balance sheet breaks down into 3 categories, assets, liabilities, and equity.

All three financial statements are comprised of elements called "line items" which provide finer levels of details within their respective financial statements.

# [Problem Statement](#section-title)
This research was conducted to implement unsupervised clustering learning techniques on financial statement line items to determine if unusual relationships exist among the account balances. Given a dataset of financial statement line items, I aim to use K-means clustering to group the data points into K clusters based on similarity. I will then analyze the cluster assignments to identify any unusual relationships or patterns in the data. Because there is no "ground truth" or "correct" number of clusters with unsupervised learning, there is no formal definition of success or a quantitative baseline by which to compare these models. The project will be considered successful if clusters can be extrapolated with clear boundaries and minimal noise encapsulated by the clusters, as determined subjectively by the researcher.


# [Target Audience](#section-title)

This project targets a borad audience which includes retail and institutional investors alike, as well as the executive leadership committees of companies. 
- **With respect to inestors:** if unique classifications can be discerned by the unsupervised learning models, the investor has a competitive edge in categorizing U.S. exchange-traded companies and can theoretically use this information to discern trends and alter their portfolio concentrations accordingly. For example, an investor who unearths that the companies with the highest revenue are also classified as companies with high interest expenses can use this knowledge to select or alter their portfolio to increase these holdings and gain a larger alpha.
- **With respect to executive leadership committes:** The executive leadership of each company are the C-Suite management who are invested in upholding or enhancing their firm’s profit margins. With the help of these machine learning techniques, the managers can uncover new relationships between various line items of their financial statements and use this to increase common financial metrics by which their stocks are traded. For example, if the CFO of a supermarket chain examines these models and identifies that companies wihtin the consumer staples sector are not classified by operating expense, he/she may chooseto direct his focus elsewhere when strategizing how to increase net profit. The actions of executive leadership affect all stakeholders within the organization, including employees and investors. Using these models to maximize financial ratios and/or refine firm strategies may increase profitability.

# [Research Approach](#section-title)

To set out in solving this research question, data was collected and cleaned from several sources and used in two unsupervised learning models: K-Means Clustering and DBSCAN. Because there are several sources and preprocessing dataframes, the below flow chart is provided for readers. 

<img src="plots/K-Means Workflow.png" alt="Alt text" width="800" height="400">

# [Data Dictionary](#section-title)

The following finanial terms are used throughout this project and are defined as follows:

| Item | Description
| --- | --- 
| **GICS** | *Global Industry Classification Standard*
| **US SEC** | *U.S. Securities and Exchange Commission* 
| **CIK** | *Central Index Key* 
| **ticker** | *abbreviation to uniquely identify publicly traded shares of a particular stock on a market.*
| **bs** | *Balance Sheet* 
| **is** | *Income Statement* 
| **cfs** | *Statement of Cash Flow* 
| **ci** | *Statement of Other Comprehensive Income* 
| **10-Q** | *Comprehensive report of financial performance submitted quarterly by all public companies* 

# [Discussion & Recommendations](#section-title)

Overall, our subsequent plans for unsupervised learning techniques showcase the potential of these technqiues to extract meaningful insights from complex financial data. Our model showcases the difficulty in fitting clustering models and deciphering financial interpretations. 

# [Software Required](#section-title)
The software required for this project are listed on the first line of code within each notebook and include: Pandas, Matplotlib, Seaborn, RESTClient, BeautifulSoup, sec-api, and SkLearn.

# [Sources](#section-title)

General:
- [GICS to cik data](https://stockmarketmba.com/listofstocksinanindustry.php)
- [GICS Industries data](https://www.msci.com/our-solutions/indexes/gics)
- [SEC ciks data](https://www.sec.gov/include/ticker.txt)
- [Financial Statement Account Balances](https://polygon.io/docs/stocks/get_vx_reference_financials)

Financial:
- [ADR](https://www.investopedia.com/terms/a/adr.asp)
- [REIT](https://www.reit.com/what-reit?gad=1&gclid=Cj0KCQjw0IGnBhDUARIsAMwFDLlE_su13-1Pvr8qxCEB8OI607EtMzpHZyz206xRF47bJAbTVCxWMAEaAg9zEALw_wcB) 
- [MLP](https://www.schwab.com/stocks/understand-stocks/mlps#:~:text=Master%20Limited%20Partnerships%20(MLPs)%20are,limited%20partners%20(the%20investors))
- [BDC](https://www.investopedia.com/terms/b/bdc.asp#:~:text=Key%20Takeaways,and%20some%20capital%20appreciation%20potential)
- [Rights](https://www.investopedia.com/investing/understanding-rights-issues/#:~:text=Defining%20a%20Rights%20Issue,-A%20rights%20issue&text=This%20type%20of%20issue%20gives,stock%20at%20a%20discount%20price.)
- [Royalty Trusts](https://www.investopedia.com/terms/r/royaltyincometrust.asp)
- [SEC ciks definition](https://www.sec.gov/edgar/searchedgar/cik)

# [Licensing](#section-title)
This project is licensed under the MIT license.