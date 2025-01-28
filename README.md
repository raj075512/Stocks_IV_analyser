
# Implied Volatility Visualizer & Stock Price Prediction Analyzer (HFT)

This project aims to provide a comprehensive toolset for analyzing **Implied Volatility (IV)** and visualizing its effects on **stock price predictions** using various datasets for **High-Frequency Trading (HFT)**. The tool uses advanced plotting techniques to visualize options data, including **Call and Put Implied Volatility** across different expiries and strike prices, making it an invaluable asset for traders, quants, and anyone interested in financial analysis.

## Features

- **Implied Volatility Visualization**: Interactive 3D plots to visualize Call and Put IV across different expiry dates and strike prices.
- **Stock Price Prediction Analysis**: Tools to analyze the correlation between implied volatility and stock price movements.
- **HFT Data Analysis**: Supports high-frequency trading datasets to analyze and visualize stock price movements, volatility, and options market data.
- **Customizable Graphs**: Users can customize the range of strike prices and time periods to analyze specific portions of the market.
- **Color-coded Heatmaps**: Color gradients (e.g., green to red) to display volatility and its trends visually.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Data Requirements](#data-requirements)
- [Features](#features)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/raj075512/Stocks_IV_analyser.git
   ```

2. Navigate into the project directory:
   ```bash
   cd implied-volatility-visualizer
   ```

3. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   ```

4. Activate the virtual environment:
   - On Windows:
     ```bash
     .\venv\Scripts\activate
     ```
   - On macOS/Linux:
     ```bash
     source venv/bin/activate
     ```

5. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. **Prepare Your Data**: Ensure that your data is formatted in a CSV file (or a DataFrame) with the following columns:
   - **Time**: Timestamp or time-related data for the options.
   - **Strike Price (STRIKE_PR)**: The strike prices of the options.
   - **Expiry Date (EXPIRY_DATE)**: The expiry date of the options.
   - **Call Implied Volatility (CE_IV)**: Implied volatility for call options.
   - **Put Implied Volatility (PE_IV)**: Implied volatility for put options.

2. **Run the Visualizer**: Execute the script for visualizing implied volatility:
   ```python
   python implied_volatility_visualizer.py
   ```

3. **Interactive Inputs**: You will be prompted to enter:
   - **ATM strike price**: Enter the At-the-money strike price.
   - **Range of points**: Enter the range of strike prices around the ATM price to filter the data.

4. **Output**: The tool will generate:
   - **3D plot**: A 3D surface plot showing the relationship between implied volatility and expiry time, strike price, and IV values.
   - **Heatmap**: A heatmap visualizing implied volatility trends across time and strike prices.

5. **Customizing Visualizations**: Adjust the plotting parameters as needed in the script (e.g., plot size, color maps, time intervals, etc.).

### Example:
```python
plot_3d_iv_atm_range(df_expiry_date_02_02_2023, 'CE_IV', 'Call IV')
```

## Data Requirements

The program works with **high-frequency trading (HFT)** datasets for options. Ensure your data is structured with the following columns:
- **Time**: The timestamp or the period of data observation.
- **Strike Price**: The strike price for the options.
- **Implied Volatility**: Both call and put implied volatilities for options.
- **Expiry Date**: The expiration date of the options.
- **Option Type**: Put or Call options for analysis.

The dataset should ideally be in a **CSV** or **Pandas DataFrame** format for easy manipulation and analysis.

## Example Data

| Time       | STRIKE_PR | EXPIRY_DATE | CE_IV   | PE_IV   |
|------------|-----------|-------------|---------|---------|
| 2025-01-28 | 41300     | 2025-02-02  | 0.12    | 0.15    |
| 2025-01-28 | 41200     | 2025-02-02  | 0.13    | 0.16    |
| 2025-01-28 | 41400     | 2025-02-02  | 0.11    | 0.14    |

## Contributing

We welcome contributions! If you'd like to contribute to the project, feel free to open an issue or submit a pull request. Here are a few ways you can help:
- Report bugs or issues you're encountering.
- Submit new features or improvements.
- Improve the documentation.

To get started, fork the repository and create a new branch for your feature or fix:
```bash
git checkout -b feature/my-new-feature
git commit -m "Add new feature"
git push origin feature/my-new-feature
```
Create a pull request with a description of your changes.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

### Additional Notes:
- **Color maps**: You can experiment with different color maps such as `'RdYlGn'`, `'viridis'`, `'coolwarm'` to change the visual output.
- **Interactive Features**: You can expand the tool to include interactive plotting libraries like **Plotly** or **Dash** for a more dynamic user experience.
- **Stock Price Predictions**: Further models (e.g., using machine learning) can be integrated to predict future stock prices based on historical volatility data.

---

This README should help anyone get started with your project and contribute effectively. Let me know if you'd like any further details added or adjustments made!
