# Looker E-commerce Analytics

An analytics portfolio project based on the [Looker E-commerce BigQuery dataset on Kaggle](https://www.kaggle.com/datasets/mustafakeser4/looker-ecommerce-bigquery-dataset). The repository contains project documentation and an executive insights report with practical recommendations.

## Repository contents

```text
.
├── README.md
├── INSIGHTS_AND_RECOMMENDATIONS.md
├── .gitignore
├── LICENSE
└── data/
    └── README.md
```

## Dataset

Download the dataset from Kaggle and keep local copies under `data/raw/`. The source includes e-commerce tables such as orders, order items, users, events, and inventory items. The supplied `ee.xlsx` workbook was used as the reference for the reported KPIs and dashboard summaries.

## Key findings

- Reported sales are approximately **$10.83M** across **125,226 orders** and **100,000 users**.
- The reported return rate is approximately **10.0%**.
- Search contributes about **70.2%** of reported sales; Organic contributes about **15.1%**.
- The inventory summary lists **490,705 items**, of which **181,759 are sold** and **308,946 remain unsold**.
- The workbook reports an average session duration of **1,044.3 minutes**. This unusually high value should be validated before it is used as a business KPI.

See [INSIGHTS_AND_RECOMMENDATIONS.md](INSIGHTS_AND_RECOMMENDATIONS.md) for interpretation, caveats, and suggested next steps.

## Data handling

Do not commit the source workbook or raw data. The workbook includes user-level fields that may contain email addresses, street addresses, and location details. `.gitignore` excludes common data exports and the local raw-data folder.

## License

The project documentation is provided under the MIT License. The Kaggle dataset remains subject to its publisher's terms; review the dataset page before redistribution.
