# README: Ultra Marathon Running Data Analysis

## Overview
This project analyzes a dataset of ultra-marathon running events spanning two centuries. The dataset includes details such as event dates, event names, distances, athlete performances, and demographic information. The primary focus is on filtering and analyzing data for 50km and 50-mile races in the USA for the year 2020.

## Dataset
The dataset used in this project is titled "TWO_CENTURIES_OF_UM_RACES.csv" from Kaggle, and contains the following columns:
- **Year of event**: The year the event took place.
- **Event dates**: The date(s) of the event.
- **Event name**: The name of the event.
- **Event distance/length**: The distance of the event (e.g., 50km, 50mi).
- **Event number of finishers**: The number of athletes who finished the event.
- **Athlete performance**: The performance time of the athlete.
- **Athlete club**: The club the athlete belongs to.
- **Athlete country**: The country of the athlete.
- **Athlete year of birth**: The birth year of the athlete.
- **Athlete gender**: The gender of the athlete.
- **Athlete age category**: The age category of the athlete.
- **Athlete average speed**: The average speed of the athlete.
- **Athlete ID**: A unique identifier for the athlete.

## Data Cleaning and Preprocessing
1. **Filtering Data**:
   - Only races in the USA for the year 2020 were considered.
   - Only races with distances of 50km or 50 miles were included.

2. **Data Transformation**:
   - The `Event name` column was cleaned to remove the country code in parentheses.
   - The `Athlete performance` column was cleaned to extract only the time (removing the 'h' suffix).
   - A new column `athlete_age` was created by subtracting the athlete's birth year from 2020.
   - Null values in the `athlete_age` column were dropped.

3. **Column Renaming and Reordering**:
   - Columns were renamed for clarity and consistency.
   - Columns were reordered to improve readability.

4. **Data Type Conversion**:
   - The `athlete_age` column was converted to an integer.
   - The `athlete_average_speed` column was converted to a float.

## Analysis and Visualizations
The following visualizations were created to analyze the data:

1. **Histogram of Race Length**:
   - A histogram showing the distribution of race lengths (50km vs. 50mi).

2. **Histogram of Race Length by Gender**:
   - A histogram showing the distribution of race lengths, colored by athlete gender.

3. **Distribution Plot of Average Speed for 50-Mile Races**:
   - A distribution plot showing the average speed of athletes in 50-mile races.

4. **Violin Plot of Average Speed by Race Length and Gender**:
   - A violin plot showing the distribution of average speeds for 50km and 50-mile races, split by gender.

5. **Scatter Plot of Athlete Age vs. Average Speed**:
   - A scatter plot with a regression line showing the relationship between athlete age and average speed, colored by gender.

## Key Findings
- The dataset contains a significant number of 50km and 50-mile races in the USA for the year 2020.
- Male athletes tend to have higher average speeds compared to female athletes in both 50km and 50-mile races.
- There is a slight negative correlation between athlete age and average speed, indicating that older athletes tend to have slightly lower average speeds.

## Dependencies
- **Pandas**: For data manipulation and analysis.
- **Seaborn**: For data visualization.
- **Matplotlib**: For additional plotting capabilities.

## Usage
To replicate this analysis, ensure you have the required libraries installed:
```bash
pip install pandas seaborn matplotlib
```
Then, run the provided Python script to load, clean, and analyze the data.

## Future Work
- Explore the impact of other variables such as athlete club or country on performance.
- Analyze trends over multiple years to identify changes in athlete performance and participation.
- Incorporate additional datasets to enrich the analysis, such as weather conditions during the events.

## License
This project is licensed under the MIT License. See the LICENSE file for details.
