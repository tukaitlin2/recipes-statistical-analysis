**By Kaitlin Tu**

## Introduction
Food.com is an online platform for users to discover, share, and review online recipes. There are a wide variety of recipes that range from simple to complex dishes. The datasets used in this analysis come from Food.com and contain information about the recipes including user interactions, preparation times, ingredient counts, and ratings.

When picking a recipe, most users first consider the amount of preparation time it would take above all. This also takes into account how many ingredients would be required for a specific recipe because this helps us understand the relationship between preparation time and the amount of ingredients needed. This relationship can help us explore whether more time-consuming recipes and ingredient-heavy recipes are generally better received by users. 

For this project, we will analyze a dataset of recipes and user reviews from Food.com. The dataset contains key features about the recipes such as preparation times, ingredients, cooking instructions, nutritional information, and user ratings. By analyzing all these aspects, we can determine how different recipe characteristics can relate to overall user satisfaction.

## Central Question

**What is the relationship between the number of ingredients, preparation time, and average recipe ratings?**

This question is relevant to home cooks and food bloggers who want to understand want makes a recipe more appealing to users. Many people have limited time and resources when preparing meals, making the balance between quality and convenience a priority when choosing a recipe. By analyzingf the number of ingredients, preparation time, and average ratinfs, I hope to discover whether more complex recipes tend to recieve higher ratings or whether simpler recipes are rated just as highly.

## Dataset Overview

The datasets used in this project are from Food.com and contain information about recipes and user interactions. The recipes dataset contains information about individual recipes and the interactions dataset contains user reviews and ratings with each recipe.

The recipe-level dataset used in this analysis contains **83,782** rows and **15** columns, where each row represents an individual recipe.

| Column | Description |
| --- | --- |
| `id` | Unique identifier for each recipe. |
| `recipe_id` | Identifier used to match reviews to recipes. |
| `name` | Name of the recipe. |
| `minutes` | Time required to prepare the recipe in minutes. |
| `n_ingredients` | Number of ingredients required. |
| `n_steps` | Number of steps required to complete the recipe. |
| `rating` | Rating given by an individual user. |
| `average_rating` | Average user rating for each recipe. |

## Data Cleaning and Exploratory Data Analysis

### Data Cleaning

### Univariate Analysis

### Bivariate Analysis

### Interesting Aggregates

## Assessment of Missingness

## Hypothesis Testing

## Framing a Prediction Problem

## Baseline Model

## Final Model

## Fairness Analysis
