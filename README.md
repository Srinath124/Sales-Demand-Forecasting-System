#Sales & Demand Forecasting System

A comprehensive machine learning solution for forecasting future sales using the Superstore Sales Dataset. This project demonstrates real-world business applications of time-series forecasting and provides actionable insights for inventory planning, cash flow management, and business decision-making.

## 📊 Project Overview

This forecasting system predicts future sales based on historical data and presents results in a business-friendly format. The solution includes:

- **Data cleaning and preparation** with time-based feature engineering
- **Multiple forecasting models** (ARIMA, SARIMA, Machine Learning)
- **Comprehensive visualizations** for non-technical stakeholders
- **Business insights** for practical decision-making

## 🎯 Business Value

Sales forecasting helps businesses:
- 📦 Plan inventory levels to avoid overstocking or stockouts
- 💰 Manage cash flow and budget allocation
- 👥 Prepare staffing requirements for peak seasons
- 📈 Identify growth opportunities and trends

## 📁 Project Structure

```
sales-forecasting/
├── data/
│   ├── raw/                    # Original Superstore dataset (download separately)
│   ├── processed/              # Cleaned and feature-engineered data (included)
│   │   ├── daily_sales_simple.csv
│   │   └── daily_sales_features.csv
│   └── README.md               # Data documentation
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   ├── 02_data_preparation.ipynb
│   ├── 03_forecasting_models.ipynb
│   ├── 04_business_insights.ipynb
│   └── 05_visualization.ipynb
├── src/                        # Python modules (required for notebooks)
│   ├── __init__.py
│   ├── data_preprocessing.py
│   ├── feature_engineering.py
│   ├── models.py
│   └── visualization.py
├── scripts/
│   └── verify_setup.py         # Setup verification script
├── outputs/
│   ├── figures/                # Saved visualizations
│   ├── forecasts/              # Prediction results
│   └── reports/                # Business insights documents
├── requirements.txt            # Python dependencies
├── .gitignore
└── README.md
```

## 🚀 Quick Start

### Prerequisites

- Python 3.8 or higher
- pip package manager
- Git (for cloning)

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Srinath124/FUTURE_ML_01.git
   cd FUTURE_ML_01
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Verify setup** (recommended):
   ```bash
   python scripts/verify_setup.py
   ```
   
   This will check:
   - ✅ Python version
   - ✅ All dependencies installed
   - ✅ Required files present
   - ✅ Data files accessible
   - ✅ Custom modules importable

4. **(Optional) Download raw data**:
   - Visit [Kaggle Superstore Dataset](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)
   - Download and place CSV in `data/raw/`
   - Only needed if you want to regenerate processed data

### Running the Analysis

**Option 1: Jupyter Notebook (Recommended)**
```bash
jupyter notebook
```
Then open and run notebooks in order: 01 → 02 → 03 → 04 → 05

**Option 2: JupyterLab**
```bash
jupyter lab
```

**Note**: The processed data files are already included, so you can start directly with notebook 03 if you just want to see the models.

## 📈 Models Implemented

### Statistical Models
- **ARIMA** (AutoRegressive Integrated Moving Average)
- **SARIMA** (Seasonal ARIMA with weekly seasonality)
- **Baseline Models** (Naive, Mean) for comparison

### Machine Learning Models
- **Linear Regression** with time-based features
- **Random Forest Regressor** for non-linear patterns

## 📊 Key Features

✅ **Data Cleaning**: Handle missing values and outliers  
✅ **Time-Based Features**: Date, month, quarter, seasonality indicators  
✅ **Lag Features**: Previous period sales for pattern recognition  
✅ **Rolling Statistics**: Moving averages and trends  
✅ **Model Evaluation**: RMSE, MAE, MAPE, R² metrics  
✅ **Business Visualizations**: Clear charts with confidence intervals  

## 🎨 Visualizations

The project generates business-friendly visualizations including:
- Historical sales trends with forecast overlay
- Category-wise and region-wise forecasts
- Seasonal patterns and decomposition
- Confidence intervals for predictions
- Error analysis and model diagnostics

## 📄 Deliverables

1. **Trained forecasting models** with performance metrics
2. **Future sales predictions** (30, 60, 90 days)
3. **Business insights report** explaining forecasts
4. **Visualizations** ready for stakeholder presentations
5. **Actionable recommendations** for business planning

## 🔍 Model Performance

| Model | RMSE | MAE | R² |
|-------|------|-----|-----|
| Linear Regression | $2,154 | $1,573 | 0.237 |
| Random Forest | $2,181 | $1,624 | 0.218 |
| ARIMA(2,1,2) | $2,741 | $1,740 | -0.183 |
| SARIMA(1,1,1)(1,1,1,7) | $2,847 | $1,806 | -0.276 |

**Best Model**: Linear Regression (lowest RMSE, positive R²)

## 💡 Business Insights

- **Seasonal Patterns**: Clear November-December peak (holiday season)
- **Weekly Trends**: Higher sales on weekdays vs weekends
- **Forecast Confidence**: ±$2,000-$3,000 daily variation expected
- **Recommendation**: Use Linear Regression model for short-term forecasts

## 🛠️ Troubleshooting

### Common Issues

**ImportError: No module named 'models'**
- Ensure you're running notebooks from the project root directory
- The notebooks automatically add `src/` to the Python path

**FileNotFoundError: data/processed/daily_sales_simple.csv**
- Verify you cloned the complete repository including data files
- Run `python scripts/verify_setup.py` to check

**Kernel dies when running models**
- Check available RAM (models need ~2GB)
- Try reducing `n_estimators` in Random Forest

**Plots not showing**
- Ensure `matplotlib` is installed: `pip install matplotlib`
- Try adding `%matplotlib inline` at the top of notebooks

### Getting Help

1. Run verification script: `python scripts/verify_setup.py`
2. Check `data/README.md` for data requirements
3. Ensure all files from Git are present (especially `src/` directory)

## 📝 License

This project is created for educational purposes as part of the Future Interns Machine Learning Task 1 (2026).

## 👥 Author

**Created by**: Srinath  
**Task**: Sales & Demand Forecasting for Businesses  
**Organization**: Future Interns  
**Repository**: https://github.com/Srinath124/FUTURE_ML_01

---

## ⚠️ Important Notes

- **Processed data included**: The `data/processed/` files are in the repository for immediate use
- **Raw data optional**: Only download if you want to regenerate processed data
- **src/ directory required**: All notebooks import from `src/` - ensure it's present
- **Run in order**: Notebooks 01-05 should be executed sequentially for best results

**Note**: This is a learning project demonstrating practical ML applications in business forecasting. The insights and recommendations should be validated with domain experts before making critical business decisions.
