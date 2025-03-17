# Analyzing Crime in Los Angeles

## 📌 Project Overview
Los Angeles, California—the City of Angels—is known for its entertainment industry, warm weather, and sprawling coastline. However, like any major city, crime is a significant concern. This project analyzes crime data from Los Angeles to uncover patterns and trends. The insights gained can help law enforcement allocate resources effectively.

## 📊 Dataset
The dataset is sourced from **Los Angeles Open Data** and contains details about reported crimes, including:

| Column         | Description |
|---------------|-------------|
| `DR_NO`       | Official file number (unique crime ID) |
| `Date Rptd`   | Date the crime was reported (MM/DD/YYYY) |
| `DATE OCC`    | Date the crime occurred (MM/DD/YYYY) |
| `TIME OCC`    | Crime occurrence time (24-hour format) |
| `AREA NAME`   | Geographic patrol division of the crime |
| `Crm Cd Desc` | Crime description |
| `Vict Age`    | Age of the victim |
| `Vict Sex`    | Victim's gender (M, F, X) |
| `Vict Descent`| Victim's descent/ethnicity |
| `Weapon Desc` | Description of the weapon used (if applicable) |
| `Status Desc` | Current crime status |
| `LOCATION`    | Street address of the crime |

## 🔍 Key Findings
- **Crime Peaks**: Most crimes occur around **10 PM**.
- **High-Risk Areas**: The **Central area** has the highest crime rate at night.
- **Victim Demographics**: Crimes are most frequently committed against individuals aged **18-25**.

## 🛠️ Technologies Used
- **Python**
- **pandas** (data manipulation)
- **matplotlib & seaborn** (data visualization)
- **NumPy** (numerical analysis)
- **Jupyter Notebook**

## 📈 Visualizations
The project includes various charts and graphs, such as:
- **Crime frequency by hour**
- **Crime distribution by area**
- **Victim age group analysis**

## 🚀 How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/LA-crime-analysis.git
   cd LA-crime-analysis
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
4. Open `crime_analysis.ipynb` and run the cells.

## 📌 Next Steps
To enhance the project, consider:
- Implementing a **machine learning model** to predict crime likelihood based on past data.
- Creating an **interactive dashboard** with `Plotly` or `Streamlit`.
- Performing **geospatial analysis** using `folium` for crime heatmaps.

## 📜 License
This project is licensed under the MIT License.

---
📬 Feel free to contribute or reach out with questions!

