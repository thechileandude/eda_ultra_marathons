# eda_ultra_marathons
Second Student Proyect
Here’s a README file tailored for your GitHub repository based on the provided Python script:

---

# Ultra Marathon Running Data Analysis

This project analyzes ultra-marathon running data from the dataset "Two Centuries of UM Races," focusing on 50km and 50mi races held in the USA during 2020. The script cleans the data, transforms it into a usable format, and generates visualizations and insights about runner performance, gender differences, age groups, and seasonal trends.

## Dataset

The data is sourced from [Kaggle: The Big Dataset of Ultra-Marathon Running](https://www.kaggle.com/datasets/aiaiaidavid/the-big-dataset-of-ultra-marathon-running). The original dataset (`TWO_CENTURIES_OF_UM_RACES.csv`) contains detailed records of ultra-marathon events worldwide.

## Prerequisites

To run this script, you’ll need the following Python libraries installed:
- `pandas`
- `seaborn`
- `matplotlib` (used implicitly by Seaborn)

You can install them using pip:
```bash
pip install pandas seaborn matplotlib
```

Ensure you have the dataset file `TWO_CENTURIES_OF_UM_RACES.csv` in the same directory as the script.

## Project Overview

The script performs the following steps:

1. **Data Import**: Loads the ultra-marathon dataset into a Pandas DataFrame.
2. **Data Cleaning**:
   - Filters for USA-based 50km and 50mi races in 2020.
   - Removes "(USA)" from event names.
   - Calculates athlete age based on birth year.
   - Drops unnecessary columns (e.g., Athlete Club, Athlete Country).
   - Removes rows with null values and resets the index.
   - Standardizes data types (e.g., integer for age, float for speed).
3. **Data Transformation**:
   - Renames columns for clarity (e.g., "Athlete average speed" to `athlete_average_speed`).
   - Reorders columns for better readability.
   - Adds a `race_month` and `race_season` column to analyze seasonal performance.
4. **Data Visualization**:
   - Histograms of race lengths and gender distribution.
   - Violin plots comparing average speeds by race length and gender.
   - Scatter plots with regression lines for age vs. speed.
5. **Insights**:
   - Average speed differences between genders for 50km and 50mi races.
   - Best and worst-performing age groups for 50mi races (with a minimum race count threshold).
   - Seasonal performance trends (Spring, Summer, Fall, Winter).

## Usage

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/ultra-marathon-analysis.git
   cd ultra-marathon-analysis
   ```
2. Place the `TWO_CENTURIES_OF_UM_RACES.csv` file in the project directory.

3. Run the script:
   ```bash
   python ultra_marathon_analysis.py
   ```
   The script will process the data and display visualizations in your Python environment. You can modify the script to save outputs (e.g., `.csv` files or images) by adding appropriate Pandas or Matplotlib commands.

## Key Findings

- **Gender Speed Differences**: Aggregates average speeds by race length and gender.
- **Top Age Groups (50mi)**: Identifies the fastest age groups with at least 20 races.
- **Slowest Age Groups (50mi)**: Identifies the slowest age groups with at least 10 races.
- **Seasonal Trends**: Compares average speeds across seasons, with a specific focus on 50mi races.

## File Structure

- `ultra_marathon_analysis.py`: The main Python script.
- `TWO_CENTURIES_OF_UM_RACES.csv`: The dataset (not included in the repo; download from Kaggle).
- `README.md`: This file.

## Visualizations

The following plots:
- Histogram of race lengths.
- Gender-specific histogram of race lengths.
- Distribution plot of average speeds for 50mi races.
- Violin plots of speed by race length and gender.
- Scatter plot with regression line for age vs. speed, split by gender.

## Future Improvements

- Add export functionality for cleaned data and visualizations.
- Expand analysis to other years or distances.
- Incorporate statistical tests for significance in speed differences.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Data provided by [Kaggle](https://www.kaggle.com/datasets/aiaiaidavid/the-big-dataset-of-ultra-marathon-running).
- Built with Python, Pandas, and Seaborn.

