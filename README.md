
# World countries development clustering

![alt text](https://github.com/ricardofariaromero/countries_clustering/blob/main/images/world_map.jpg)

Using data about development indicators in the world, we have created a clustering model that based on these parameters classify each country in five categories:

    - Highly underdeveloped country
    - Underdeveloped country
    - Emerging country
    - Developed country
    - Highly developed country

The database used counts with 10 features and 167 records.


## Variables and EDA

For this study the following variables has been analyzed:

    - country: name of the country.
    - child_mort: death of children under 5 years of age per 1000 live births.
    - exports: exports of goods and services per capita. Given as %
     of the GDP per capita.
    - health: total health spending per capita. Given as %age of GDP per capita.
    - imports: imports of goods and services per capita. Given as % of the GDP per capita.
    - Income: net income per person.
    - Inflation: the measurement of the annual growth rate of the Total GDP.
    - life_expec: the average number of years a new born child would live if the current mortality patterns are to remain the same.
    - total_fer: the number of children that would be born to each woman if the current age-fertility rates remain the same.
    - gdpp: the GDP per capita. Calculated as the Total GDP divided by the total population.

Regarding the variables, we analyzed the distribution and boxplots for each of them:

![alt text](https://github.com/ricardofariaromero/countries_clustering/blob/main/images/numerical.png)

![alt text](https://github.com/ricardofariaromero/countries_clustering/blob/main/images/categorica.png)

## Python Libraries and algorithm

The following libraries were used during this project:

    - Pandas
    - Seaborn
    - Matplotlib
    - Scikit-learn (KMeans algorithm)

## Analysis and results

By using the elbow method we determined the clusters to applied selecting 5 as the number:

![alt text](https://github.com/ricardofariaromero/countries_clustering/blob/main/images/elbow.png)

Later on, we graph each cluster Vs each of the indicators to get insights on them:

![alt text](https://github.com/ricardofariaromero/countries_clustering/blob/main/images/clusters.png)

* Cluster 0: countries with old population and low births rates. They characterized for high exports, but also high imports, making them consumptions/production societies. Their GDP and income per person is greatly higher than other countries and their inflation rates are low. We will renamed this group "Highly developed countries"
* Cluster 1: countries with moderately high child mortality and relatively young populations with an stable birth rate. These societies are considered relatively poor that tend to import and export at the same level. Their income per person and GDP is low and their inflation high, making them prom to economical crisis. We will renamed this group "Underdeveloped countries"
* Cluster 2: Old population countries with the lowest birthrate, a characteristic often found in ancient countries like european nations. With a moderately high income and controlled inflation, tend to expend a great deal of monety on health a feature found on "Wellfare states". We will renamed this group "Developed countries"
* Cluster 3: countries with and increasing quality of life: high life expectancy, low child mortality and average birthrate. Their income and GDP is average and inflation very variable with imports and export levels very similar. We will renamed this group "Emerging countries".
* Cluster 4: this groups the biggest amount of countries, with the worsts living conditions: high child mortality and low life expectancy. The birth rate is greatly higher than other countries, almost 4 kids per family, the double of the rest of the groups. Their income and GDP is the lowest of all, and tend to import more than their produce. These are countries in economical crisis with high inlation rates. We will renamed this group "Highly underdeveloped countries".
        
## Credits

All code and development performed by [Ricardo Faría](https://www.linkedin.com/in/ricardo-e-faria-romero/?locale=en_US) 
