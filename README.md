<h1 align='center'> World Happiness Index 2023 Analysis </h1>

**Insert happy**

The Global Happiness Index through 2023 delivers an extensive and current analysis of happiness measures and the determinants affecting global well-being. Aimed at furnishing critical insights for decision-makers,
scholars, and those keen on exploring the nuances of happiness and welfare across the globe, 
this dataset serves as a pivotal resource for comprehending the complexities of contentment and quality of life internationally. The propose of this Analysis is to both shows the variables that is correlated to higher happiness score, 
and the estimated causal effect that each numerical variable on happiness score. 

##  The DataFrame

| Column | Description |
| ----------- | ----------- |
| country | The name of the country |
| region | The geographic region or continent |
| happiness_score | A measure reflecting overall happiness |
| gdp_per_capita | A measure of Gross Domestic Product per capita |
| social_support | A metric measuring social support |
| healthy_life_expectancy | A measure of years of healthy life expectancy |
| freedom_to_make_life_choices | A measure of freedom in life choices |
| generosity | A metric reflecting generosity |
| perceptions_of_corruption | A measure of perception of corruption within a country |

## Tools 

It Was used the Jupyter Notebook (Python IDE) to host the analysis, and was used the following Python Libraries:

- Pandas is a library providing high-performance, easy-to-use data structures, and data analysis tools. It is particularly suited for working with tabular data (similar to Excel spreadsheets).

- NumPy offers comprehensive mathematical functions, random number generators, linear algebra routines, Fourier transforms, and more.

-  Matplotlib a plotting library that is highly customizable and capable of creating static, animated, and interactive visualizations in Python.

- Seaborn built on top of Matplotlib, Seaborn is a statistical data visualization library designed to make visualization a central part of exploring and understanding data.

- SciPy is built on NumPy and provides additional functionality with submodules for optimization, integration, interpolation, eigenvalue problems, algebraic equations, differential equations, and others.

-  Statsmodels focuses on statistical models, hypothesis tests, and data exploration. Statsmodels is great for conducting statistical tests and inferences.

- Plotly.express a high-level API for creating figures. It is designed to make the creation of complex, beautiful visualizations easy with a simple syntax, that can be manipulated live.

- DoWhy a library for causal inference that simplifies the use of advanced causal inference techniques. It provides a principled way to model your assumptions and estimate causal effects based on those assumptions, making it easier to apply causal analysis in practice.



## Propose of the Analysis

### Bussiness Problem

The Foreign Relation Minister was invited to an Internacional Wellbeing Conference, and he was selected to do to a presentation of what makes a country happier. The Cabinet Sub Secretary for the Foreign Relations Minister, contacts the Data Science Manager of the Federal Government Secretary and explain the demand.

The Manager contacts you, a Data Scientist Intern, the Manager knows that you are still learning, and you think that he's crazy by choosing you, but he explains that it is your chance to show what you made of, and you accept the challenge (just like if you had another choice).

Another thing that the Manager mentioned, is that the Sub Secretary needs this report ASAP, so you must hurry! 😢

### Project Objects

The objective is to investigate the factors associated with national happiness scores and provide insights that can inform the development of public policies aimed at promoting societal wellbeing. The project advocates for a comprehensive approach to policymaking, wherein economic prosperity, physical health, social cohesion, and individual freedoms are considered collectively in fostering national happiness. By recognizing the interplay between these variables, governments, organizations, and individuals can devise more effective strategies for cultivating happier and more resilient societies.

## Analysis

### EDA

> The region that shows the biggest range between the minimum and maximum on Happiness Score is the Middle East and North Africa. And the countries that reveals this diference are neighbors. Israel has a Score of 7.473, and Lebanon with 2.392. a diference of 5.081. With these scores, Israel is the Fourth happiest country in 2023, and Lebanon is  the penultimate.**Insert israel and lebanon and map of countries**

> the top 10 and least 10 countries sorted by happiness score. **Insert top and least**

> It shows that except the North America and ANZ, the Western Europe, that are the "happier" regions, and Sub-Saharar  Africa and South Asia, are the "less happy" regions, all the others regions presents a similar happiness score. **Insert happiness mean** 

> Happiness Score: The distribution appears to be slightly left-skewed, indicating that more countries have happiness scores above the mean. Most countries cluster around the middle to high range of the happiness scale.
GDP per Capita: This variable shows a broad spread with a peak towards the lower end, suggesting that while many   countries have lower GDP per capita, there's a significant tail extending towards higher values. This indicates    economic disparities across countries.
Social Support: The distribution is slightly left-skewed, similar to happiness score, implying that most countries report higher levels of social support.
Healthy Life Expectancy: Shows a somewhat normal distribution but with a slight left skew. It suggests that while  many countries enjoy moderate to high life expectancy, a few countries are significantly lagging behind.
Freedom to Make Life Choices: The distribution is more uniform but slightly peaks towards the higher end,indicating that many countries enjoy a relatively high level of freedom.
Generosity: Appears to be right-skewed, with most countries showing lower levels of generosity but with a long tail towards higher generosity scores.
Perceptions of Corruption: Heavily right-skewed, with many countries perceiving low levels of corruption, but with a long tail indicating that some countries perceive very high levels of corruption. **Insert Distribuition**

> Ir shows the Pearson's correlation used in the heat map of all numeric variables **Insert heatmap**

> The plot above shows all the strongest correlation varialbes with the Hapiness Score. It appers that the Social Support, GDP per Capita, and Freedom to Make Life Choises do a strong positive effect in Happiness Score. Showing this four variables may be the cause of the happiness score variance.**Insert scatter**

### Statistical Inference

> Ordinary Least Squares
It is a statistical method used to estimate the parameters of a linear regression model. This method seeks to minimize the sum of the squares of the differences between the observed values of the dependent variable and those predicted by the linear model.
Principles of OLS Regression
Multiple Linear Model: OLS applies to models where the relationship between the dependent variable and one or more independent variables is linear. The model can be expressed as:
𝑌=𝛽0+𝛽1𝑋1+𝛽2𝑋2+…+𝛽𝑛𝑋𝑛+𝜀
Minimization of the Sum of Squared Residuals: The objective of OLS regression is to find the values of β that minimize the sum of the squared residuals (differences between the observed and predicted values). Mathematically, this is expressed as: 
min∑𝑖=1𝑛(𝑌𝑖−𝑌̂ 𝑖)2 

**Insert OLS**

> R-squared: 0.856 means that 85.6% of the variability in happiness score are explained by the included independent  variables. This is quite high, suggesting the model does a good job at explaining happiness scores.
Adj. R-squared: 0.838 adjusts the R² based on the number of predictors in the model, giving a more accurate measure for models with multiple variables. Still, it's quite high, reinforcing the model's effectiveness.
The OLS does not Shows the Causal, but we can tell that high Social Support, GDP per Capita, Healthy life Expectancy, and Freedom to make life Choices are correlated to a higher Happiness Score
This analysis suggests an approach to the development of public policies, where economic, physical health, social  support, and individual freedom are considered together in promoting national happiness. This perspective can guide governments, organizations, and individuals in implementing more effective strategies for building happier and more resilient societies.

## Causal Inference

### Dowhy Library

**Insert Dowhy**

Modeling

The first step in causal inference is to model your problem, typically using a Directed Acyclic Graph (DAG). A DAG helps in visualizing the causal relationships among variables.

Notation: Let's denote treatment by T, outcome by Y, and any confounders (variables that influence both treatment and outcome) by X or W.

𝑋→𝑇→𝑌 

Identification

Once you have a model, the next step is identifying the causal effect you're interested in estimating. This usually involves assumptions like ignorability, which states that there are no unmeasured confounders. The Average Treatment Effect (ATE) is a common target for identification.

ATE Definition: The average difference in outcome if all units had received the treatment versus if none had.

ATE=𝐸[𝑌|𝑑𝑜(𝑇=1)]−𝐸[𝑌|𝑑𝑜(𝑇=0)]

Here, E[ ] denotes the expected value, and do( ) represents a do-operation, indicating intervention by setting T to a particular value.
Estimate

After identifying the causal effect, the next step is to estimate it from the data. This involves statistical methods that adjust for the confounders to isolate the effect of the treatment from other influences.

denote the propensity score, then the ATE can be estimated by matching or weighting observations by

𝑒(𝑋)=𝑃(𝑇=1|𝑋)(𝑒(𝑋).

Refutation

The final step in the causal inference process is to test the robustness of your estimated effect. DoWhy offers several refutation methods, like adding a random common cause or replacing the treatment with a random (placebo) treatment.

Placebo Treatment Test: If replacing the actual treatment with a placebo does not significantly change the outcome, it raises questions about the causal relationship.

**Insert effect on happiness**


## Conclusion

Moreover, the project employs causal inference techniques to assess the impact of various factors on happiness scores. The results indicate that social support and freedom to make life choices exert the most substantial positive effects on happiness, followed by economic indicators like GDP per capita and health-related factors such as healthy life expectancy. Additionally, perceptions of corruption, while only moderately correlated with happiness scores, demonstrate a notable causal effect.

The robustness of these findings is validated through refutation tests, which evaluate the sensitivity of causal estimates to alternative scenarios.

In summary, the project underscores the complex nature of happiness and emphasizes the significance of considering a diverse array of factors in both policymaking and personal decision-making processes. By prioritizing social support, individual freedoms, economic prosperity, health outcomes, and integrity in governance, societies can aspire to enhance overall wellbeing and foster greater happiness among their citizens.
