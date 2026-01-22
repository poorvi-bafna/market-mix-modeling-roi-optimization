# Market Mix Modeling (MMM) for Marketing ROI Optimization

This project implements a **Market Mix Model (MMM)** using regularized regression techniques to measure the impact of multiple marketing channels on sales and to estimate their relative marginal Return on Investment (ROI).

## 📌 Project Overview
The primary objective of this notebook is to provide a data-driven framework for marketing budget allocation by:
* **Understanding Sales Drivers:** Analyzing how various marketing spends influence overall sales.
* **Capturing Consumer Behavior:** Modeling "Adstock" (carryover effects) and "Saturation" (diminishing returns) to reflect real-world advertising dynamics.
* **Quantifying Contribution:** Measuring the incremental contribution of each advertising channel.
* **Optimizing ROI:** Enabling strategic decisions for budget allocation based on simulated ROI.

## 📊 Dataset Description
The model utilizes a comprehensive dataset (referenced as `marketing_campaign_data.xlsx`) containing:
* **Target Variable:** Sales ($).
* **Marketing Spend Channels:** SMS, Newspaper, Radio, TV, and Internet.
* **Control Variables:** Unit Price, POS/Supply data, and Macroeconomic factors (Consumer Price Index, Consumer Confidence Index, Producer Price Index).
* **Temporal Data:** Observations spanning from 2010 to 2017.

## 🛠 Tools & Techniques
* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, SciPy.
* **Modeling:** Ridge Regression pipeline with Standard Scaling.
* **Feature Engineering:**
    * **Adstock Transformation:** Accounts for the lingering effect of past advertising on current sales.
    * **Saturation (Hill Function):** Models the point where additional spend yields diminishing returns.
    * **Log Transformations:** Applied to Sales and Price to model elasticities and stabilize variance.

## 📈 Key Insights & Strategic Recommendations
The analysis provides actionable business recommendations:
* **High Performers:** **Newspaper advertising** shows high ROI; recommended to **increase investment**.
* **Moderate Performers:** **Radio** shows moderate effectiveness; recommended for **selective investment**.
* **Underperformers:** **SMS, TV, and Internet** show low, negligible, or negative ROI (indicating saturation or over-investment); recommended to **reduce or pause spend** and optimize targeting before reinvesting.

## 🚀 How to Use
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    ```
2.  **Ensure you have the dataset:** Place `marketing_campaign_data.xlsx` in the same directory as the notebook.
3.  **Install dependencies:**
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn scipy
    ```
4.  **Run the analysis:** Open and execute `Market_Mix_Modeling_for_Marketing_ROI_Optimization.ipynb` in Jupyter or Google Colab.

## 📁 Repository Structure
* `Market_Mix_Modeling_for_Marketing_ROI_Optimization.ipynb`: Complete Python pipeline for MMM.
* `marketing_campaign_data.xlsx`: Dataset
* `README.md`: Project documentation.
