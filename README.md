# Online Retail: Python Data Cleaning and Analysis

My first end-to-end Python data analysis project, completed in Google Colab.

## Project objective

Explore a public retail dataset, investigate data quality issues,
document cleaning decisions, visualise sales patterns, and explain
how unusual transactions can affect analytical findings.

## Tools

- Python
- pandas
- Matplotlib
- Google Colab

## Dataset

The UCI Online Retail dataset contains 541,909 invoice lines from
a UK-based online retailer.

Source: https://archive.ics.uci.edu/dataset/352/online+retail

Each row represents an invoice line, rather than a complete order.
The notebook downloads the dataset directly from UCI.

## What I did

- Checked missing values, data types, exact duplicates, quantities,
  prices, and cancellation entries.
- Created separate analysis tables while preserving the original data.
- Documented filtering rules and duplicate-removal assumptions.
- Visualised monthly sales, product rankings, countries, and customers.
- Investigated large transactions and related cancellation entries.
- Compared product rankings with and without two investigated entries.
- Validated the selected data and ran the notebook from top to bottom.

## Key findings

- November 2011 had the highest monthly gross merchandise sales
  value in the original view: £1,453,265.98.
- May had the largest month-to-month percentage increase: 43.54%.
- Two large positive entries had evidence of subsequent offsets.
  Excluding them changed the top 10 product rankings, while the
  four leading products remained unchanged.
- In the sensitivity view, the UK contributed 84.41% of sales value.
- Customer IDs covered 85.21% of sensitivity-view sales value.
- The top 10 identified customers contributed 16.80% of
  identified-customer sales value.

## Analysis scope and limitations

Analysis covers December 2010 to November 2011. The partial month
of December 2011 is excluded.

The original gross-sales view excludes cancellations, non-positive
quantities and prices, identified non-merchandise codes, and exact
repeated rows.

The sensitivity view additionally excludes two investigated positive
entries with evidence of offsets. Country and customer analyses use
this view; monthly findings use the original gross-sales view.

These measures are not net revenue or profit. Cancellations and
adjustments were not comprehensively reconciled. Exact duplicate
removal was an assumption, and missing customer IDs limit customer
analysis. The available period cannot establish recurring seasonality.

## How to run

1. Download the project notebook from this repository.
2. Open https://colab.research.google.com/.
3. Choose File → Upload notebook and select the downloaded file.
4. Choose Runtime → Run all.

An internet connection is required to download the source dataset.
