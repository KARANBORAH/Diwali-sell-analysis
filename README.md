


This kaggle Notebook performs exploratory data analysis (EDA) and visualization using a dataset related to State-wise amounts. The project focuses on:

    Grouping data by states

    Aggregating total amounts per state

    Visualizing results using bar plots

    A plan for mapping visualizations on a geographic map

🔧 Technologies Used

    Python 3

    Pandas – data manipulation

    Matplotlib & Seaborn – data visualization

    Jupyter Notebook – interactive environment for data analysis

📂 Project Structure

.
├── diwagali.ipynb        # Main notebook for data analysis
├── README.md             # Project documentation
└── data/                 # (Expected) Folder for CSV or dataset used in analysis

📈 Features

    Aggregation of transaction/amount data by state

    Barplot visualization of state-wise amount using Seaborn

    Code snippet for plotting geographical maps (planned/needed)

📌 Future Improvements

    Add a map-based visualization using libraries like Plotly, Folium, or Geopandas

    Clean and preprocess other columns (e.g., Marital_Status as categorical labels)

    Provide insights and business recommendations from the analysis

📥 How to Run

    Clone this repository or download the .ipynb file

    Place the dataset (if required) in the appropriate path

    Open the notebook in Jupyter or Google Colab

    Run all cells to reproduce the results

✅ Example Code

amount_state = df.groupby(['State'], as_index=False)['Amount'].sum().sort_values(by='Amount', ascending=False)
sns.set(rc={'figure.figsize':(30,10)})
sns.barplot(x='State', y='Amount', data=amount_state)

📍 Mapping Suggestion

Use this snippet (with plotly.express or folium) to plot a choropleth map:

import plotly.express as px
fig = px.choropleth(amount_state, 
                    locations='State', 
                    locationmode='country names', 
                    color='Amount', 
                    color_continuous_scale='Viridis')
fig.show()


