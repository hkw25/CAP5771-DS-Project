# CAP5771 Project: Air Quality Inequality

## Project Overview
This project investigates the correlation between environmental hazards (Air Quality Index), socioeconomic status (Median Income, Demographics), and public health outcomes (Cancer Incidence Rates) at the U.S. county level. 

## Repository Structure
- `data/`: Contains raw CSV/Excel data files from the EPA, CDC, and US Census.
- `diary/`: Project documentation covering problem formulation, data acquisition, and reflections.
- `aqi_project.ipynb`: The primary executable Jupyter Notebook containing data cleaning, database schema creation, and exploratory data analysis.
- `aqi_project.db`: The SQLite relational database.
- `data_dictionary.pdf`: Documentation of all database variables and data types.
- `requirements.txt`: Python environment dependencies.

## Project Problem Formulation

### 1. What type of problem would you need to solve?
Air quality inequality across different income levels in the United States.
* **a. Prediction:** We could predict future air quality levels for a region based on historical pollution data and socioeconomic factors such as income level and population density.
* **b. Classification:** Low pollution vs. high pollution. Environmentally advantaged vs. disadvantaged areas based on air quality thresholds and income levels.
* **c. Exploration:** We would explore patterns and relationships between Median household income and pollution levels, Poverty rates and long-term air quality exposure, and Geographic clustering of high-pollution, low-income communities.
* **d. Recommendation:** The system could recommend priority areas for increased air quality monitoring and environmental regulations.
* **e. Decision Support:** We could support policy and planning decisions by helping officials decide where to allocate environmental resources and which communities should receive intervention first.

### 2. How will you obtain the data?
We will use two publicly available datasets. For Air Quality Data we will use the EPA Air Quality System. For Socioeconomic & Demographic Data we will use the U.S. Census Bureau (American Community Survey).

### 3. What is the central question you want to answer using data?
Do lower-income communities experience consistently worse air quality than higher-income communities, and where are these disparities most severe?

### 4. Why is this question important within its context?
Air pollution is directly linked to asthma, heart disease, and reduced life expectancy. If poorer communities are disproportionately exposed to pollution, this represents an environmental justice issue.

### 5. What makes this project unique compared to other similar projects?
Combines environmental data with socioeconomic inequality, not just pollution levels alone. Focuses on disparity and fairness, not just averages.

### 6. What variables are required, and why are they essential?
From the Air Quality Dataset, the variables we would need are PM2.5 concentration (Key health-relevant pollutant), AQI (Standardized measure for comparison), Geographic location (Required to merge datasets), Time (year/month). From Census Dataset Median, the variables we would need are household income, Poverty rate, and Population density (Controls for urban vs. rural effects).

### 7. What would a meaningful or successful answer look like?
A successful outcome would include clear statistical evidence showing whether income correlates with air quality. Also an identification of specific regions or communities facing the worst conditions.

### 8. Who would use the results, and how would they benefit?
Potential users include environmental policymakers, advocacy groups, and urban planners. The benefits of this would be better allocation of resources and increased awareness of environmental inequality.

### 9. Is this problem realistic, given typical resource constraints?
Yes, very realistic since the data is free and well-documented and analysis can be done using standard tools like Python and pandas.

---

## How will you track your progress during the semester?
We will organize our workflow using Agile development, breaking into 5 sprints.
* **Sprint 1:** Setup and Data Acquisition
* **Sprint 2:** Data Cleaning
* **Sprint 3:** Exploratory Analysis and Statistics
* **Sprint 4:** Visualization and Mapping
* **Sprint 5:** Final Polish

---

## Part 2: The Heilmeier Catechism

### 1. What are you trying to do? Articulate your objectives using absolutely no jargon.
We are trying to find out whether people who live in lower-income communities are exposed to worse air quality than people in higher-income communities, and where those differences are the largest.

### 2. How is it done today, and what are the limits of current practice?
Today, air quality and income data are usually looked at separately. Many reports focus on national or state averages, which can hide local differences. This makes it difficult to see which specific communities are most affected.

### 3. What is new in your approach, and why do you think it will be successful?
Our approach combines air quality data and income data at the same geographic location so they can be compared directly. By looking at these two data points together, we can show patterns and disparities that are not apparent when the data is analyzed separately.

### 4. Who cares? If you are successful, what difference will it make?
Public health officials and environmental advocacy groups care about this problem. If we are successful, our results can help them identify which communities need cleaner air and more monitoring.

### 5. What are the risks?
The main risks are incomplete data or missing measurements in some areas. These issues could limit how precise our conclusions can be.

### 6. How much will it cost?
The project will use free, publicly available datasets and open source software.

### 7. How long will it take?
Should definitely be able to complete within an academic semester.

### 8. What are the mid-term and final "exams" to check for success?
The mid-term checks would be successfully merging air quality and income datasets while showing some pollution differences across income levels. The final exam checks would be clear evidence supporting or rejecting the idea that lower-income communities face worse air quality. Also would like to include a final report that clearly communicates the results and implications of the project.
