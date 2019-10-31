# Evolution of Net Remittance

![alt text](https://raulincadet.github.io/remittance.png)
### Research Question
Since many people in low income-level countries emigrate to look for a better income, remittances inflow in these countries might be high. However, people in these countries also send remittances to their relatives in other countries, for several reason such as the education of their children. Thus, instead of considering only inflow of remittances in these countries, it is essential to compare the net remittances balance of low-income level countries with the ones of middle and high income level countries. Thus, our project is specific to the following question. Does the mean of the net remittance higher for low-income level countries, compared to other groups of countries?

### Data cleaning
We import the modules that will be used in the project. Pandas will be used to read the microsoft excel files. Matplotlib will be used to realize the graphic. The data used to answer the research question are provided on the website of the [World Bank](https://data.worldbank.org/). The three datasets used provide data about inflow of remittances, outflow of remittances, and historical threshold for classification of countries according to their income-level.

We verify if there are some inaccurate records in the data, and we clean them when they are identified. We remove unecessary rows and columns; we also change the type of missing data that are string to NaN float type. In spite that all the three dataset are provided by the same institution, there are some differences in the name of the countries. We identify the differences in the spelling of the name of some countries from a dataset to another. Then, we correct them to have the same spelling for the three dataset.

### Comparison of the net flow of remittances by income-level
This section compares the mean of net remittance by group of countries, classified in terms of income-level. The classification used is the one of the World Bank, as indicated in the preambule. The World Bank use the [Atlas method](https://datahelpdesk.worldbank.org/knowledgebase/articles/378832-what-is-the-world-bank-atlas-method), to realize this classification.

To do this comparison, we:
* Create a new data frame which is the difference between inflow and outflow of remittances, for each country, for each year where data are available. The new data generated is the net remittance for each country, by year.
* Create a function that:
     * Groups net remittance by class, according to the income-level classification, for a year. This operation requires that we account for both the net remittance data frame and the classification data frame.
     * Calculate the mean of net remittance, by group of countries.
     * Iterate the first two previous operation for all years where data are available.
     * Return a data frame with the mean of the net remittance, by group of countries, for each year.
     
The previous process is repeated to compute the mean of net remittance per capita. In this case, after computing the net remittance by country, it is divided by the population (for each country and by year).

### Discussion
Figure 1 shows that, although low-income level countries are still net remittance receivers, considering the mean of net the mean amount they receive tends to decrease. However, the net remittance may tend to decrease because of a decrease of the total population in low-income level countries. Some countries may switch from low-income level group to another. In this case, the population of low-income level country group may decrease. When considering the mean of the population by group of countries, we observe (see figure 2) that it tends to decrease since the end of the 1990s.

Thus, instead of considering the mean of net remittance, we plot the mean of net remittance per capita. Figure 3 shows that although the mean of net remittance per capita is increasing in low-income-level countries, it is lower when compared to lower-middle and upper middle income-level groups. 
