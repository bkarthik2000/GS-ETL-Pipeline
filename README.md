

## Project Overview

A production-ready ETL pipeline that:
- Reads messy CSV data from multiple sources (online orders, store orders, mobile orders)
- Handles real data quality issues: inconsistent formats, test data, duplicates
- Cleans and standardizes customer IDs, prices, and dates
- Outputs clean CSV files ready for analysis
- Includes logging, error handling, and data quality checks

## Setup

### Prerequisites
- Python 3.8+
- Java 11 or 17 (recommended for Spark)

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/bkarthik2000/GS-ETL-Pipeline.git
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Verify Spark is working:
   ```bash
   pyspark
   ```
   You should see the Spark shell start. Type `exit()` to quit.


```

## Sample Data

The CSV files in `data/raw/` contain realistic data quality issues you'll fix:

- **Inconsistent customer IDs**: Some are numbers (`12345`), some have prefixes (`CUST_12345`)
- **Messy prices**: Mix of `$12.99` and `12.99` formats
- **Test data**: Records with `TEST` in various fields that need filtering
- **Duplicates**: Same order appearing multiple times
- **Inconsistent dates**: Different date formats across files




## Quick Start

After running the completed pipeline:

```bash
spark-submit main.py
```

Successful output will be in `data/processed/orders/orders.csv` with a summary report in `logs/`.

