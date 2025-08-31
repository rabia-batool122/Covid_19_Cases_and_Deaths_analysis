# Overview

The objective of this analysis is to provide clear and data-driven insights into the impact of Covid-19 across different regions of the world. By examining reported deaths and cases, the study highlights the countries and continents most affected during the pandemic. Through comparative visualizations, the analysis aims to:

Identify the top 10 countries with the highest reported deaths and cases by continent.

Compare the scale of reported deaths and cases across countries within each continent.

Contrast total deaths against total reported cases at a continental level to better understand relative impact.

This structured approach offers a comprehensive perspective on how Covid-19 affected populations differently across regions, supporting further discussions on global health response and preparedness.

## The Analysis

## 1. Top 10 Countries for Most Reported Deaths By Continent During Covid-19

To find the Major Number of Deaths in Countries by the Order of continent, this analysis is performed to provide insights into Top 10 most countries of each continent for Deaths during Covid-19.

View my notebook with detailed steps here:
[2_plot_deaths_country.ipynb](1_COVID-19_C_and_D/2_plot_deaths_country.ipynb)

### Visualization

```python
df_plot_Africa.plot(kind='bar',
                    x='location', 
                    y='total_deaths', 
                    color=palette )


plt.show()
```

#### Results

![Visualization of Most Reported Deaths Top 10 Countries](images/Total_Deaths_By_Countries/Death_By_Countries_Africa.png)

### Insights
 - South Africa and Egypt dominate death counts: South Africa leads with 845K reported deaths, followed by Egypt at 465K. Together, they account for more than half of the deaths among the top 10 African countries, highlighting stark disparities in mortality across the continent.

 - Algeria is a distant third: With 153K deaths, Algeria has significantly fewer reported deaths compared to South Africa and Egypt, showing a steep drop-off after the two leading countries.

 - Nigeria, Sudan, and Morocco occupy the mid-tier: Nigeria (92K), Sudan (77K), and Morocco (72K) make up the middle range, with numbers much closer to each other and forming a secondary cluster of high mortality among African nations.

 - Cameroon, Ethiopia, Kenya, and Congo have substantially lower reported deaths: These countries report fewer than 50K deaths each, with Democratic Republic of Congo at the lowest among the top 10 with just 23K, underscoring a significant variance within the continent.


 ## 2. Top 10 Countries for Most Reported Deaths by Continent During Covid-19

 To find the Major Number of Cases in Countries by the Order of continent, this analysis is performed to provide insights into Top 10 most countries of each continent for Cases during Covid-19.


 View my notebook with detailed steps here:
 [3_reported_cases_country.ipynb](1_COVID-19_C_and_D/3_plot_reported_cases_country.ipynb)

 ### Visualization

 ```python
 df_plot_Asia.plot(kind='bar', 
                  x='location', 
                  y='total_cases',
                  color=palette)

plt.show()
 ```

#### Results

![Visualization of Most Reported Cases by Top 10 Countries](images/Total_Cases_By_Countries/Cases_Countries_Asia.png)

### Insights
 - India stands far ahead of all Asian countries: With 211.5 million reported cases, India has an enormous lead over every other country in Asia—surpassing the next highest, Iran, by more than fivefold.

 - Iran, Turkey, Saudi Arabia, and Pakistan form a secondary cluster: Each of these countries has between 28.3M and 38.3M reported cases, showing a significant concentration of cases in the region, though all are drastically lower than India.

 - Bangladesh and China maintain sizable but lower case numbers: Bangladesh (24.2M) and China (18.9M) stand apart from the top five, still reporting substantial cases but at a noticeably reduced magnitude.

 - Iraq, Philippines, and Qatar round out the list with the lowest numbers: These countries each report fewer than 15M cases, highlighting a steep descending trend within the top 10 and illustrating the wide disparity in reported cases across Asian nations.

## 3. Comparison of Reported Deaths and Cases by Top 10 Countries of Each Continent.

In this Comparative-Analysis of Deaths and Cases Reported by Top 10 Countries of each Continent, Data has been visualized to give a bigger picture of how many cases and deaths have been reported side-by-side.

View my notebook with detailed steps here:
[4_plot_compare_deaths_and_cases.ipynb](1_COVID-19_C_and_D/4_plot_compare_deaths_and_cases.ipynb)

### Visualization
```python
fig, ax = plt.subplots(1, 2)

sns.barplot(data=df_plot_Europe_cases, 
            x='location', 
            y='total_cases', 
            ax=ax[0], 
            hue='location', 
            palette='dark:b_r')

plt.show()
```

#### Results
![Visualizing the comparison of Deaths and Cases by Countries of the given Continent](images/Comparison_countries_Europe.png)

### Insights
 - Russia leads in reported cases, but the UK tops deaths: Russia recorded the highest number of cases (near 100M), while the United Kingdom saw the highest number of deaths (over 6M), showing a disparity between infection rates and mortality figures.

 - Spain and the UK have high case counts: Both Spain and the United Kingdom report over 40M cases each, positioning them among the most affected European nations in terms of total Covid-19 infections.

 - Italy and France rank high in both cases and deaths: Italy and France appear among the top five for both total cases and deaths, indicating a significant impact in both infection rates and fatalities.

 - Western European countries dominate the upper ranks: Countries such as Belgium, Germany, and the Netherlands consistently rank among the top in both cases and deaths, highlighting the pandemic’s intensive spread and mortality in Western Europe.


## 4. Comparison of Total Deaths and Total Cases by Continent.

In the given analysis total death rate of each continent is compared to the total reported cases rate in order to understand the context of Death rate as compared to Reported Cases rate.

View my notebook with detailed steps here:
[5_plot_compare_deaths_and_cases_continent.ipynb](1_COVID-19_C_and_D/5_plot_compare_deaths_and_cases_continent.ipynb)

### Visualization
```python
fig, ax = plt.subplots(1, 2)

sns.barplot(data=df_continent, 
            x='continent', 
            y='total_cases', 
            ax=ax[0], 
            hue='continent' , 
            palette='dark:b_r')

plt.show()
```

#### Results
![Visualizing the comparison of Deaths and Cases by Continent](images/Continent_Comparison.png)

 
### Insights
 - Europe was the global epicenter in both metrics. It recorded the highest absolute number of confirmed cases (approaching 600 million) and, most strikingly, the highest death toll by a significant margin, exceeding 25 million.

 - Asia's high case count did not translate to a proportionally high death toll. While Asia had a case volume nearly matching Europe's, its reported fatalities were less than half, suggesting potential differences in demographics, healthcare capacity, reporting methods, or pandemic response effectiveness.

 - North America experienced a severe impact relative to its population. It reported the third-highest case count but the second-highest number of deaths, indicating a high case fatality ratio compared to other continents like Asia and South America.

 - Africa reported the lowest figures for both cases and deaths among all continents. This is a notable observation given its large population, potentially pointing to factors like a younger demographic, possible underreporting, or different public health approaches.

 - Oceania successfully suppressed the virus for a longer period. The data shows it had the second-lowest case and death numbers, reflecting the effectiveness of its initial isolation-based containment strategies and lower population density.
