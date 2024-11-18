# Mining_Lab2_Task

An e-commerce company wants to analyze the monthly sales data across different regions to
predict seasonal trends. The dataset includes categorical and numeric variables, as well as missing
values.
data = pd.DataFrame({ 'Region': ['North', 'South', 'East', 'West', 'North', 'South', 'East', 'West',
'North', 'South', 'East', 'West'], 'Month': ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct',
'Nov', 'Dec'], 'Sales': [200, 300, None, 400, None, 500, 600, 700, None, 800, 900, None],
'Discount': [5, 10, 15, None, 20, 25, None, 30, 35, None, 40, 45], })

Task Requirements:
• Replace missing sales values with the mean sales of that specific region.
• Fill missing discount values with 0.
• Apply MinMax scaling to the Sales column and standardize the Discount column.

Task 2
A hospital has collected medical records of patients, including test results for various biomarkers.
Some values are missing, and several attributes have outliers due to errors in measurement.
data = pd.DataFrame({

'PatientID': range(1, 11),
'BloodSugar': [110, 190, None, 95, 300, 115, 87, 305, 92, None],
'Cholesterol': [200, 185, 300, 280, None, 195, 230, None, 210, 250],
'BP_Systolic': [120, 130, 250, 110, 160, 140, None, 180, None, 190],
'BP_Diastolic': [80, 85, 100, 70, 120, 90, None, 95, 105, 110],
})

Task Requirements:
• Replace missing values in BloodSugar and BP_Systolic with the median values of their
respective columns.
• For any BloodSugar value above 200, replace it with the mean value.
• Detect and handle outliers in the Cholesterol column by capping values above 250 to 250.
• Normalize the BP_Systolic and BP_Diastolic columns so each row has a unit norm.
• Create a binarized feature indicating whether each patient’s Cholesterol is above or below
220.

NOTE: USE loc() AND where() FUNCTIONS IN THIS TASK (not for everything).

Task 3
A weather agency collects daily weather data, including temperature, humidity, and wind speed.
Data from some sensors has unusually high values and missing entries.
data = pd.DataFrame({
'Day': range(1, 11),
'Temperature': [25, None, 45, 39, 42, 38, None, 46, 50, None],
'Humidity': [55, 75, None, 95, 105, 115, None, 65, 60, 85],
'WindSpeed': [5, 15, None, 20, 35, 50, None, 55, 60, None]
})

Task Requirements:
• Replace missing values in Temperature with the median, in Humidity with the mean, and
in WindSpeed with 0.
• Cap Humidity values above 100 at 100.
• Apply binarization to Temperature, setting any value above 40 as “High” and 40 or below
as “Normal.”
• Standardize WindSpeed to have a mean of 0 and standard deviation of 1.

Task 4
A telecom company wants to analyze call data for a customer satisfaction project. The dataset
includes information on call duration, data usage, and customer feedback. Some data points are
missing, and certain values seem unusually high.

data = pd.DataFrame({
'CustomerID': range(1, 11),
'CallDuration': [15, None, 45, 10, 120, None, 35, 50, 20, 90],
'DataUsage': [1.2, 1.5, 3.0, None, 2.5, None, 5.0, 7.5, None, 6.0],
'SatisfactionScore': [4, 3, None, 5, None, 2, 1, 4, None, 5]
})

Task Requirements:
1. Replace missing CallDuration values with the median of the column.
2. For any DataUsage above 5 GB, replace it with the mean DataUsage.
3. Standardize CallDuration to have a mean of 0 and standard deviation of 1.
4. Normalize DataUsage so each row has a unit norm.
5. Create a new column using lambda that labels SatisfactionScore as "Low" if it’s below 3,
"Medium" if it’s 3, and "High" if it’s above 3.

Task 5
A research study gathers data on participants’ height, weight, and age for an analysis of health
trends. Some entries contain missing values and others may have been entered incorrectly.
data = pd.DataFrame({
'ParticipantID': range(1, 11),
'Height': [160, None, 170, 165, None, 180, None, 175, 160, 155],
'Weight': [60, None, 80, 85, None, 95, 100, None, 70, 65],
'Age': [25, None, 45, 50, None, 30, 35, None, 40, 20]
})

Task Requirements:
1. Replace missing Height values with the average Height for participants over 30 years old.
2. Replace Weight values over 90 with the median of the Weight column.
3. Normalize Height and Weight to have a unit length for each row.
4. Apply binarization to Age, setting values above 30 as "Older" and 30 or below as
"Younger".
5. Use lambda to categorize Weight into "Underweight" if below 70, "Normal" if 70-85, and
"Overweight" if above 85.
