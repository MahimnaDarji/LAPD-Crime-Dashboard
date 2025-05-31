# LAPD-Crime-Dashboard
This project is about building an interactive crime analytics dashboard using over 900,000 records from the Los Angeles Police Department (LAPD). The goal was to help users explore crime trends, patterns, and victim demographics in a visual and easy-to-understand way. The data was cleaned, categorized, and filtered to allow users to focus on what matters most to them — be it a specific location, type of crime, or demographic group.

The dashboard was developed using Streamlit and Python and integrates Google Drive for seamless data loading, making it scalable and deployment-friendly even with such a large dataset.

## What Was Done:

Data Collection & Cleaning: Crime data was loaded from Google Drive using a direct download link, handled via the gdown Python library. Missing values were filled with appropriate placeholders like “Unknown” or “N/A,” and entries with invalid coordinates were removed to ensure accurate mapping.

Categorization of Crimes: Crimes were grouped into four categories—Violent Crimes, Property Crimes, Cyber/White-Collar Crimes, and Miscellaneous—based on their descriptions. This categorization helps in understanding the nature and severity of criminal activities in different areas.

Interactive Filters: The sidebar offers multiple filters like crime type, victim gender, descent, age range, area, and date range. These filters dynamically update all the visuals on the dashboard, allowing users to narrow down data and explore it based on their needs.

## Spatial Visualization:

Heatmap: A heatmap is displayed using the Folium library to show crime intensity by location, making it easy to identify high-crime hotspots in LA.

Cluster Map: A stratified sampling method was applied when the data volume was too high. A cluster map displays crime locations grouped based on proximity, which helps in reducing clutter and improving clarity.

## Temporal Visualization:

Calendar Heatmap: Shows the number of crimes per day, giving users a feel for the busiest days.

Monthly Trends by Crime Type: A line chart shows how each type of crime changes month-by-month.

Weekly Trends: Weekly crime trends are also displayed with options to filter by crime type.

## Demographic Breakdown:

Pie Charts: Gender and age distribution of victims are visualized using pie charts. Victim age is grouped into bins like 0–18, 19–30, etc.

Bar Charts: Distribution by descent is shown using bar charts, giving insight into which ethnic or racial groups are most affected.

Dashboard Performance: A stratified sampling method ensures that charts load smoothly even when the dataset is large. By limiting data points while maintaining proportional representation, we solved the common performance bottleneck associated with large datasets.

Deployment Strategy: Google Drive integration was used to host the data file, enabling easy access and avoiding memory issues during deployment. This makes the dashboard portable and usable across different systems without having to store the dataset locally.

## Impact:

The dashboard makes it easier for the public, journalists, or city planners to understand crime patterns in Los Angeles.

Law enforcement can use it to identify hotspots and deploy resources more effectively.

The visual breakdown allows stakeholders to track changes over time and assess the effectiveness of policies or interventions.

## Technologies Used:

## Languages & Libraries:
Python, Pandas, Streamlit, Plotly, Folium, Calplot, gdown

## Visualization:
Heatmaps (Folium), Cluster Maps (Folium), Line Charts (Plotly), Pie Charts (Plotly), Bar Charts (Plotly), Calendar Heatmap (Calplot)

## Data Handling & Transformation:
Streamlit Sidebar Widgets, Stratified Sampling, Custom Category Mapping

## Deployment & Integration:
Google Drive (for data hosting), Streamlit (for web interface), gdown (for data download), streamlit-folium (to render Folium maps in Streamlit)
