# data-512-homework_2

**Goal**

The goal of this assignment is to explore the concept of bias in data using Wikipedia articles. This assignment considers articles on political figures from different countries. I combine a dataset of Wikipedia articles with a dataset of country populations, and use a machine learning service called ORES to estimate the quality of each article. I also analyze how the coverage of politicians on Wikipedia and the quality of articles about politicians varies among countries. My analysis consists of a series of tables that show:

The countries with the greatest and least coverage of politicians on Wikipedia compared to their population.

The countries with the highest and lowest proportion of high quality articles about politicians.

A ranking of geographic regions by articles-per-person and proportion of high quality articles.

**Liscense MIT**

**Data Used**
The Wikipedia [Category:Politicians by nationality](https://en.wikipedia.org/wiki/Category:Politicians_by_nationality) was crawled to generate a list of Wikipedia article pages about politicians from a wide range of countries. This data is in the GitHub as politicians_by_country_SEPT.2022.csv.
The population data is available in CSV format as population_by_country_2022.csv from GitHub. This dataset is drawn from the world population data sheet published by the Population Reference Bureau.

**APIs Used**
[ORES](https://www.mediawiki.org/wiki/ORES) -  machine learning tool that can provide estimates of Wikipedia article quality

[Info](https://www.mediawiki.org/wiki/API:Info) - ORES requires a specific revision ID of a specific article to be able to make a label prediction. You can use the API:Info request to get a range of metadata on an article, including the most current revision ID of the article page.



