# 💊 Drug Sales Forecasting & Safety Stock Estimation

This project uses **machine learning** to predict seasonal drug sales and recommends **safety stock levels** based on historical data. It's built using Python, Pandas, and Scikit-learn with a Random Forest Regressor model.

---

## 📌 Features

* Predicts drug sales for a selected season.
* Estimates safety stock levels using historical sales data.
* Evaluates prediction quality using **Mean Absolute Error (MAE)**.
* Provides easy customization for new datasets.

---

## 📁 Dataset

The project expects a CSV file named `drug_sales.csv` with the following format:

```
Drug,Winter,Spring,Summer,Autumn,Monsoon
Paracetamol,100,120,150,110,130
Ibuprofen,90,85,80,95,100
...
```

Each row represents a drug and its sales in different seasons.

---

## ⚙️ How It Works

1. **Data Preprocessing**:

   * The data is reshaped to a long format.
   * Seasons and drug names are label-encoded.

2. **Model Training**:

   * A `RandomForestRegressor` model is trained on sales data using seasons as input.

3. **Prediction & Evaluation**:

   * Users input a season, and the model predicts sales for all drugs.
   * MAE is calculated to evaluate model performance.

4. **Safety Stock Calculation**:

   * For each drug, safety stock is calculated using the formula:
     `Safety Stock = Average Sales + (1.5 × Standard Deviation of Sales)`

---

## 🚀 Usage

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/drug-sales-forecasting.git
cd drug-sales-forecasting
```

### 2. Install Dependencies

```bash
pip install pandas scikit-learn
```

### 3. Add Your Dataset

Place your `drug_sales.csv` file in the project directory.

### 4. Run the Script

```bash
python predict_sales.py
```

You'll be prompted to enter a season (e.g., `Winter`, `Summer`), and the script will display:

* Predicted sales for each drug
* Recommended safety stock levels
* Prediction quality (Good / Needs Improvement)

---

## 🧪 Example Output

```
Enter the season (Winter, Spring, Summer, Autumn, Monsoon): Summer

Recommended Safety Stock Levels:
Drug: Paracetamol, Recommended Safety Stock Level: 168.23
Drug: Ibuprofen, Recommended Safety Stock Level: 121.50

Prediction Quality: Good (based on MAE percentage)
```

---

## 🛠️ Technologies Used

* Python
* Pandas
* Scikit-learn
* Random Forest Regressor

---

## 📈 Future Improvements

* Incorporate more features (e.g., region, temperature).
* Add interactive dashboard using Streamlit.
* Enable prediction based on multiple input factors.

---

## 📬 Contact

Created by **Yujesh Shyam** – Feel free to reach out for collaboration or questions!

---
