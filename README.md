<h1 align='center'> World Happiness Index 2023 Analysis </h1>

<img src="C:\Users\Davi Samora\Downloads\Default_Create_a_image_to_my_project_that_analysis_what_make_a_2.jpg">


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

The analysis starts with an E.D.A, where it seem the relationship between the variables, the variables statistics of the, the top 10 and least 10 countries sorted by happiness score. *** Insert Image***

Ir shows the Pearson's correlation used in the heat map of all numeric variables *** Insert Image***



## Conclusion

Moreover, the project employs causal inference techniques to assess the impact of various factors on happiness scores. The results indicate that social support and freedom to make life choices exert the most substantial positive effects on happiness, followed by economic indicators like GDP per capita and health-related factors such as healthy life expectancy. Additionally, perceptions of corruption, while only moderately correlated with happiness scores, demonstrate a notable causal effect.

The robustness of these findings is validated through refutation tests, which evaluate the sensitivity of causal estimates to alternative scenarios.

In summary, the project underscores the complex nature of happiness and emphasizes the significance of considering a diverse array of factors in both policymaking and personal decision-making processes. By prioritizing social support, individual freedoms, economic prosperity, health outcomes, and integrity in governance, societies can aspire to enhance overall wellbeing and foster greater happiness among their citizens.
