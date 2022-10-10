# data-512-homework_2

**Goal**

The goal of this assignment is to explore the concept of bias in data using Wikipedia articles. This assignment considers articles on political figures from different countries. I combine a dataset of Wikipedia articles with a dataset of country populations and use a machine learning service called ORES to estimate the quality of each article. I also analyze how the coverage of politicians on Wikipedia and the quality of articles about politicians varies among countries. My analysis consists of a series of tables that show...

The countries with the greatest and least coverage of politicians on Wikipedia compared to their population.

The countries with the highest and lowest proportion of high-quality articles about politicians.

A ranking of geographic regions by articles-per-person and proportion of high-quality articles.

**Research Implications**

The first thing I learned is that the per capita coverage rankings can be misleading as population size may have impacted the findings more than a normalizing technique should. Population size can sometimes be 0.0 million in our dataset which makes countries with that listed population at the top of the list of articles per capita. Small countries in general are at the top of the list of articles per capita for both only quality articles and all articles. Large countries, on the other hand, tend to be at the top of the list of lowest total articles per capita. The lowest total articles per capita list of quality articles includes some countries we know to have questionable journalism standards. It is also hard to believe the Wikipedia peer-reviewed articles are following the same standards from country to country which leads to bias in the data.

1. What biases did you expect to find in the data (before you started working with it), and why?

I expected to find that non-English speaking countries would have fewer peer-reviewed articles as Wikipedia was started as a Western knowledge-capturing website. I also believe that smaller countries may not have enough data to accurately depict the quality and quantity of their Wikipedia pages.

2. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might create biased or misleading results, due to the inherent gaps and limitations of the data?

If we are using this data to predict the article quality of different article titles, we may have very problematic results. The features country and region create many biases and we may predict an article is of bad quality just because of the country or region of the article. That is extremely unfair to the writer of the article and a more holistic approach would be necessary for answering this type of question.

3. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might still be appropriate and useful, despite its inherent limitations and biases?

If we are using this data to predict country based on region, population, and article title this may not be problematic. There is still some bias as people live in countries where their name is not common, but overall the affects of this bias would not cause damaging real-world effects.

**Liscense MIT**

**Data Used**

The Wikipedia [Category:Politicians by nationality](https://en.wikipedia.org/wiki/Category:Politicians_by_nationality) was crawled to generate a list of Wikipedia article pages about politicians from a wide range of countries. This data is in the GitHub as politicians_by_country_SEPT.2022.csv.
The population data is available in CSV format as population_by_country_2022.csv from GitHub. This dataset is drawn from the world population data sheet published by the Population Reference Bureau.

**APIs Used**

[ORES](https://www.mediawiki.org/wiki/ORES) -  machine learning tool that can provide estimates of Wikipedia article quality

[Info](https://www.mediawiki.org/wiki/API:Info) - ORES requires a specific revision ID of a specific article to be able to make a label prediction. You can use the API:Info request to get a range of metadata on an article, including the most current revision ID of the article page.

**Files Created**

Identify all countries for which there are no matches and output a list of those countries, with each country on a separate line called:
wp_countries-no_match.txt

Consolidate the information country, region, population, article_title, revision_id, and article_quality into a single CSV file called:
wp_politicians_by_country.csv

**List of articles we were not able to gather sources**

Unable to retrieve prediction for  Prince Ofosu Sefah

Unable to retrieve prediction for  Harjit Kaur Talwandi

Unable to retrieve prediction for  Abd al-Razzaq al-Hasani

Unable to retrieve prediction for  Kang Sun-nam

Unable to retrieve prediction for  Segun “Aeroland” Adewale

Unable to retrieve prediction for  Nhlanhla “Lux” Dlamini

**Known Issues**

The population of several countries is listed at 0.0 million. Although the population of these countries are small, we know they are not 0.0 million. However, when performing the analysis, when dividing by population the articles per person ratio can be infinity for these incorrect population representations.


