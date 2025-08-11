Title: Nutrition food and carbon footprint 

Overview
This Power BI dashboard empowers users to explore and evaluate meals based on nutritional value, carbon footprint, and dietary preferences. It integrates exploratory data analysis (EDA), DAX-driven metrics, and interactive filtering to support informed, health-conscious, and eco-friendly decisions.

Objectives
- Visualize nutritional metrics (energy, macronutrients, fiber)
- Assess environmental impact via carbon footprint
- Enable filtering by region, meal type, category, and allergens
- Highlight fiber-rich, low-carbon, and balanced meals
- Support personalized meal discovery


Key DAX Measures
- AvgEnergy = AVERAGE(Food[Energy_kcal])
- TotalCarbon = SUM(Food[Carbon_kgCO2e])
- LowCarbonMeals = CALCULATE(COUNTROWS(Food), Food[Carbon_kgCO2e] < 1)
- SustainabilityScore = [LowCarbonMeals] / [TotalMeals]
- FiberBins = SWITCH(TRUE(), ...) (for histogram bucketing)

Filters & Slicers
- Region
- Meal_Type (Breakfast, Lunch, Dinner, Snack)
- Category (Veg, Non-Veg, Vegan)

Validation & Testing
- Missing values handled via logic-based imputation
- Outliers flagged and optionally excluded
- DAX measures tested for edge cases
- Visuals validated for responsiveness and clarity


