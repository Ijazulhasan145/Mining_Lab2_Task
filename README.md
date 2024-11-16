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
