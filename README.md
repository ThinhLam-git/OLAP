# Hanoi Housing Data Analysis Project

## Overview
This project provides a comprehensive analysis of the Hanoi housing market using a dataset of over 82,000 property records. The analysis includes data mining, visualization, machine learning models, and business intelligence solutions using Microsoft's SSIS and SSAS technologies.

## Dataset Description
- **Dataset**: Hanoi real estate data (`Dataset_BDS_HANOI.csv`, `VN_housing_dataset.csv`)
- **Size**: 82,498 records
- **Time Period**: Starting from August 2020
- **Coverage**: Properties across various districts in Hanoi, Vietnam

### Data Fields
- **Ngày**: Date of listing
- **Địa chỉ**: Property address
- **Quận**: District
- **Huyện**: Ward/Commune
- **Loại hình nhà ở**: Type of housing (street-facing, alley house, etc.)
- **Giấy tờ pháp lý**: Legal documentation status
- **Số tầng**: Number of floors
- **Số phòng ngủ**: Number of bedrooms
- **Diện tích**: Area (m²)
- **Dài**: Length (m)
- **Rộng**: Width (m)
- **Giá/m2**: Price per square meter (VND millions)

## Project Structure

```
├── Dataset_BDS_HANOI.csv          # Original dataset
├── VN_housing_dataset.csv         # Processed dataset
├── DATA MINING/                   # Data mining and machine learning
│   ├── data_mining.ipynb         # Main analysis notebook
│   ├── data_mining.html          # HTML version of analysis
│   ├── cleaned_data.csv          # Cleaned dataset
│   └── processed_VN_housing_dataset.csv
├── EXCEL/                        # Excel analysis files
│   ├── cau1.xlsx - cau12.xlsx    # Analysis questions 1-12
├── SSIS/                         # SQL Server Integration Services
│   ├── SQLQuery1.sql            # SQL queries
│   └── SSIS/                    # SSIS project files
└── SSAS/                        # SQL Server Analysis Services
    ├── Query.mdx               # MDX queries
    └── SSAS/                   # SSAS project files
```

## Analysis Components

### 1. Data Mining & Machine Learning (`DATA MINING/`)
The Jupyter notebook contains comprehensive analysis including:
- **Data Preprocessing**: Handling missing values, data type conversion, normalization
- **Exploratory Data Analysis**: Statistical summaries and data distribution analysis
- **Correlation Analysis**: Pearson correlation coefficients between variables
- **Machine Learning Models**:
  - Linear Regression
  - Decision Tree
  - Random Forest
  - XGBoost
- **Model Evaluation**: MAE, MSE, R² metrics for model comparison

### 2. Excel Analysis (`EXCEL/`)
Contains 12 different analysis questions (`cau1.xlsx` through `cau12.xlsx`) covering various aspects of the housing market data.

### 3. Data Warehouse Solutions
#### SSIS (SQL Server Integration Services)
- **ETL Processes**: Data extraction, transformation, and loading
- **Data Integration**: Combining and cleaning data from multiple sources
- **Package.dtsx**: Main SSIS package for data processing

#### SSAS (SQL Server Analysis Services)
- **Data Warehouse Cubes**: Multidimensional data modeling
- **Dimensions**:
  - `DIM DATE.dim`: Time dimension
  - `DIM HOUSE.dim`: House properties dimension
  - `DIM LEGAL DOCUMENTS.dim`: Legal documentation dimension
- **Cube**: `House DW.cube` for OLAP analysis
- **MDX Queries**: Advanced analytical queries

## Key Insights

The analysis provides insights into:
- **Price Trends**: Housing price patterns across different districts
- **Market Segmentation**: Analysis by property type, legal status, and location
- **Predictive Modeling**: Machine learning models to predict housing prices
- **Spatial Analysis**: Geographic distribution of properties and prices
- **Time Series Analysis**: Market trends over time

## Technology Stack

- **Python**: Data analysis and machine learning (pandas, scikit-learn, XGBoost)
- **Jupyter Notebook**: Interactive data analysis environment
- **Excel**: Business analysis and visualization
- **SQL Server**: Database management
- **SSIS**: Data integration and ETL processes
- **SSAS**: Multidimensional analysis and OLAP cubes
- **MDX**: Multidimensional query language

## Getting Started

### Prerequisites
- Python 3.x with pandas, numpy, scikit-learn, XGBoost
- Jupyter Notebook
- Microsoft Excel
- SQL Server (for SSIS/SSAS components)
- SQL Server Data Tools (SSDT)

### Running the Analysis

1. **Data Mining Analysis**:
   ```bash
   cd "DATA MINING"
   jupyter notebook data_mining.ipynb
   ```

2. **Excel Analysis**:
   - Open individual `.xlsx` files in the `EXCEL/` folder
   - Each file contains specific analysis questions and visualizations

3. **SSIS Package**:
   - Open `SSIS/SSIS.sln` in SQL Server Data Tools
   - Deploy and execute the SSIS packages

4. **SSAS Cube**:
   - Open `SSAS/SSAS.sln` in SQL Server Data Tools
   - Deploy the SSAS database and process the cube
   - Use `Query.mdx` for sample MDX queries

## Data Quality Notes

- The dataset contains some missing values in fields like floor count, dimensions, and legal documentation
- Price data is in Vietnamese Dong (triệu = millions)
- Geographic data includes both district and ward-level information
- Property types include both street-facing properties and alley houses

## Contributing

This project serves as a comprehensive example of real estate data analysis combining multiple Microsoft BI tools with Python-based data science approaches.

## License

This project is for educational and research purposes. Please ensure compliance with data usage regulations when working with real estate data.

---
*Last Updated: August 2025*