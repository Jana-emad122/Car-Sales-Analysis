# Car Sales Analysis

## Project Overview

This project analyzes a cleaned dataset of vehicle sales transactions
and turns the data into business-focused insights and interactive
dashboards.

The project covers the full analysis flow:

-   Data preparation and quality checks
-   Exploratory Data Analysis (EDA)
-   Bivariate and multivariate analysis
-   Feature engineering
-   Excel / dashboard-oriented analysis
-   Power BI dashboarding
-   KPI validation
-   Business insights and recommendations

## Dataset

The cleaned dataset contains:

-   **558,799** vehicle-sale records
-   **22** variables
-   **97** distinct makes
-   **38** state codes
-   **3** transmission categories, including Unknown

Main variables include:

`Year`, `Make`, `Model`, `Trim`, `Body`, `Transmission`, `State`,
`ConditionValue`, `Odometer`, `MMR`, `SellingPrice`, `SaleDate`,
`VehicleAge`, `PriceToMMR`, and `PriceDifference`.

Source file:

`cleaned_car_sales.xlsx`

## Data Preparation

The uploaded cleaned dataset shows the following quality checks:

-   **72** missing values in `Odometer`
-   **0** full-row duplicate records
-   **0** duplicate IDs
-   **72** records marked with `Odometer_999999_flag`
-   The current `Odometer` field contains no `999999` values
-   **4** records are marked with `SellingPrice_1_flag` and still have
    `SellingPrice = 1`

Feature engineering present in the cleaned dataset includes:

-   `VehicleAge`
-   `PriceToMMR`
-   `PriceDifference`
-   `SellingPrice_1_flag`
-   `Odometer_999999_flag`

> Note: The original raw dataset and the Python cleaning notebook/script
> were not included, so undocumented transformations cannot be
> reconstructed from the uploaded files.

## Exploratory Data Analysis

Key descriptive findings:

-   Average Selling Price: **\$13,611**
-   Median Selling Price: **\$12,100**
-   Average MMR: **\$13,769**
-   Median MMR: **\$12,250**
-   Ford has the largest record count with **93,553** records.
-   Chevrolet follows with **60,197** records.
-   Nissan follows with **53,946** records.
-   Automatic transmission represents **85.17%** of the dataset, with
    **475,904** records.

## Relationship Analysis

The main correlations with Selling Price are:

  Variable           Correlation with Selling Price
  ---------------- --------------------------------
  MMR                                     **0.984**
  Vehicle Age                            **-0.587**
  Odometer                               **-0.591**
  ConditionValue                          **0.313**

### Interpretation

-   **MMR and Selling Price** have a very strong positive association.
-   **Vehicle Age and Selling Price** have a negative association; older
    vehicles generally have lower selling prices.
-   **Odometer and Selling Price** have a negative association.
-   **ConditionValue and Selling Price** have a moderate positive
    association.

These are descriptive relationships and do not establish causation.

## Multivariate Analysis

The project also examines Selling Price across combinations of:

-   Vehicle Age
-   Condition Value

Within age bands, higher condition bands generally correspond to higher
average selling prices. Across age bands, average selling price
generally decreases as vehicles become older.

Example:

-   Vehicles aged **0--2 years**
-   Condition band **40--49**
-   Average Selling Price ≈ **\$21,094**

## Dashboards

### Excel

The presentation includes a dashboard-oriented view built from the
cleaned dataset, including:

-   KPI cards
-   Top makes by record count
-   Transmission mix
-   Key relationships with Selling Price

### Power BI

The Power BI dashboard contains KPIs and visuals covering:

-   Average Selling Price
-   Average MMR
-   Average Odometer
-   Maximum ConditionValue
-   Record Count
-   Average odometer by color
-   Condition value trend by make
-   MMR and Selling Price by state
-   Selling Price by transmission
-   Selling Price by state
-   Selling Price by trim

## KPI Validation

The Power BI displayed KPIs reconcile with the cleaned dataset at the
displayed precision:

  KPI                           Dataset   Power BI
  ----------------------- ------------- ----------
  Average Selling Price     \$13,611.36     13.61K
  Average MMR               \$13,769.38     13.77K
  Average Odometer            68,201.07     68.20K
  Max ConditionValue                 49         49
  Record Count                  558,799   558.799K

Independent Excel KPI validation was not possible because the original
Excel dashboard/source output was not included in the uploaded
materials.

## Business Insights

1.  **MMR is closely aligned with Selling Price**\
    The correlation of 0.984 indicates a very strong positive
    association in this dataset.

2.  **Vehicle age matters**\
    Selling Price generally decreases across older vehicle-age bands.

3.  **Mileage shows a negative relationship with price**\
    Odometer has a correlation of -0.591 with Selling Price.

4.  **Condition provides additional information**\
    ConditionValue has a positive correlation of 0.313 with Selling
    Price, and higher condition bands generally show higher prices
    within age groups.

## Business Recommendations

Based on the observed patterns:

-   Use **MMR as a core pricing reference** when reviewing transaction
    prices.
-   Include **vehicle age** in pricing and inventory analysis.
-   Evaluate **vehicle age and condition together** rather than
    independently.
-   Use dashboard filters to compare vehicles by **state, make,
    transmission, color, and trim**.

These recommendations are limited to relationships visible in the
uploaded data. They do not assume information about margins, demand,
business costs, or inventory constraints.

## Project Files

Recommended project structure:

``` text
Car-Sales-Analysis/
│
├── cleaned_car_sales.xlsx
├── Car_Sales_Analysis_Final_Presentation.pptx
└── README.md
```

## Tools

-   Excel
-   Power BI
-   Python / data-analysis workflow

## Scope and Limitations

This README is based on the uploaded cleaned dataset and final
presentation.

The following were not available for independent verification:

-   Original raw dataset
-   Python cleaning notebook/script
-   Original Excel dashboard/source workbook

Therefore, this project documents the transformations, findings, and
dashboard values that are directly supported by the uploaded materials.
