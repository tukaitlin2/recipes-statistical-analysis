**By Kaitlin Tu**

## Introduction
Food.com is an online platform for users to discover, share, and review online recipes. There are a wide variety of recipes that range from simple to complex dishes. The datasets used in this analysis come from Food.com and contain information about the recipes including user interactions, preparation times, ingredient counts, and ratings.

When picking a recipe, most users first consider the amount of preparation time it would take above all. This also takes into account how many ingredients would be required for a specific recipe because this helps us understand the relationship between preparation time and the amount of ingredients needed. This relationship can help us explore whether more time-consuming recipes and ingredient-heavy recipes are generally better received by users. 

For this project, we will analyze a dataset of recipes and user reviews from Food.com. The dataset contains key features about the recipes such as preparation times, ingredients, cooking instructions, nutritional information, and user ratings. By analyzing all these aspects, we can determine how different recipe characteristics can relate to overall user satisfaction.

## Central Question

**What is the relationship between the number of ingredients, preparation time, and average recipe ratings?**

This question is relevant to home cooks and food bloggers who want to understand want makes a recipe more appealing to users. Many people have limited time and resources when preparing meals, making the balance between quality and convenience a priority when choosing a recipe. By analyzing the number of ingredients, preparation time, and average ratings, I hope to discover whether more complex recipes tend to recieve higher ratings or whether simpler recipes are rated just as highly.

## Dataset Overview

The datasets used in this project are from Food.com and contain information about recipes and user interactions. The recipes dataset contains information about individual recipes and the interactions dataset contains user reviews and ratings with each recipe.

The recipe-level dataset used in this analysis contains **83,782** rows and **21** columns, where each row represents an individual recipe.

| Column | Description |
| --- | --- |
| `id` | Unique identifier for each recipe. |
| `name` | Name of the recipe. |
| `minutes` | Time required to prepare the recipe in minutes. |
| `n_ingredients` | Number of ingredients required. |
| `n_steps` | Number of steps required to complete the recipe. |
| `average_rating` | Average user rating for each recipe. |
| `time_category` | Category assigned to a recipe based on its preparation time. |

## Data Cleaning and Exploratory Data Analysis

### Data Cleaning
The data cleaning process involved several key steps:

1. **Merging the datasets:** Performed a left merge between recipes and interactions datasets using their corresponding recipe IDs to preserve all recipes in the original dataset.

2. **Handling zero ratings:** Replaced any ratings of 0 with NaN because these values are missing rather than actual user ratings.

3. **Calculating average ratings:** Calculated the average rating for each recipe and stored it in a column called 'average_rating'.

4. **Creating a recipe-level dataset:** Combined average ratings with the original recipe information so each row is an individual recipe.

5. **Handling invalid values:** Replace nonpositive values in 'minutes' and 'n_ingredients' columns with NaN because these values do not represent realistic recipe characteristics.

6. **Categorizing preparation times:** Created a new column called 'time_category' to group recipes based on their preparation time.

7. **Extracting nutritional information:** Separated the 'nutrition' column into seven different columns representing calories, total fat, sugar, sodium, protein, saturated fat, and carbohydrates.

After completing these steps, our resulting dataset contains 
**83,782 rows and 21 columns**.

Below is a sample of the cleaned dataset. For readability purposes, I removed columns containing lengthy text and lists have been excluded from the displayed table. These columns are not relevant to the central question where I chose to primarily focus on preparation time, number of ingredients, and average recipe ratings. The displayed dataset contains **16** columns out of the reported **21**.

<style>
.scroll-table {
    width: 100%;
    overflow-x: auto;
}

.scroll-table table {
    width: max-content;
    white-space: nowrap;
}

.scroll-table th,
.scroll-table td {
    vertical-align: top;
    padding: 8px 12px;
}
</style>

<div class="scroll-table" markdown="1">

| name                                 |     id |   minutes |   contributor_id | submitted   |   n_steps |   n_ingredients |   average_rating | time_category   |   calories |   total_fat |   sugar |   sodium |   protein |   saturated_fat |   carbohydrates |
|:-------------------------------------|-------:|----------:|-----------------:|:------------|----------:|----------------:|-----------------:|:----------------|-----------:|------------:|--------:|---------:|----------:|----------------:|----------------:|
| 1 brownies in the world    best ever | 333281 |        40 |           985201 | 2008-10-27  |        10 |               9 |                4 | 30-60 min       |      138.4 |          10 |      50 |        3 |         3 |              19 |               6 |
| 1 in canada chocolate chip cookies   | 453467 |        45 |          1848091 | 2011-04-11  |        12 |              11 |                5 | 30-60 min       |      595.1 |          46 |     211 |       22 |        13 |              51 |              26 |
| 412 broccoli casserole               | 306168 |        40 |            50969 | 2008-05-30  |         6 |               9 |                5 | 30-60 min       |      194.8 |          20 |       6 |       32 |        22 |              36 |               3 |
| millionaire pound cake               | 286009 |       120 |           461724 | 2008-02-12  |         7 |               7 |                5 | 60-120 min      |      878.3 |          63 |     326 |       13 |        20 |             123 |              39 |
| 2000 meatloaf                        | 475785 |        90 |          2202916 | 2012-03-06  |        17 |              13 |                5 | 60-120 min      |      267   |          30 |      12 |       12 |        29 |              48 |               2 |

</div>

### Univariate Analysis

### Bivariate Analysis

### Interesting Aggregates

## Assessment of Missingness

## Hypothesis Testing

## Framing a Prediction Problem

## Baseline Model

## Final Model

## Fairness Analysis
