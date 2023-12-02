# UN Datathon 2023 

Looking at the UN Sustainable Development Goals, the challenge was to create a localized solution to help reach goals in one (or more) of six key areas - food systems, energy access and affordability, digital connectivity, education, jobs and social protection, and climate change and biodiversity. “Create an innovative data solution which tackles local sustainable development challenges, and which leverages one or several of the six transitions.” The solution needed to be local, but applicable/scalable globally. 

[United Nations' Six Transitions](https://unsdg.un.org/resources/six-transitions-investment-pathways-deliver-sdgs)

# Project Overview

Our team looked to apply Factor Analysis, Structural Equation Modeling, and Composite Measuring to analyze the impact of homegrown food. 

In our initial Structural Modeling, we looked at four key categories: purpose (longterm commitment to cultural values), emotional attributes (associations made by residents to backyard gardening), functional benefits (tangible features), and experiential qualities (intangible features). We then looked to apply 'Activation Levers' to each of these concepts. These Levers were quantifiable metrics through which we could realize our progress and rank in each of our four key categories. When complete, it looked like this:

## Structural Equation Model v1[^1]

| Key Category  | Concept       | Product Levers       | Price Levers        | Place Levers        | People Levers       | Proximity Levers    |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | 
| Purpose       | Sustainability, Fight Against Hunger  | Dedicated Garden Space  | Cost of planting a sq. ft. of garden  | Available Garden Space  | Garden Outreach Programming  | # of Garden Centers (proximity)  | 
| Emotional     | Positive Mental Health, Pride  | Tastes Good  | Cost of Mental Health  | Sun Exposure  | Sentiment  | Walk Score  |
| Functional    | Food Quality, Food Variety  | Nutritional Value  | Cost of Growing a Plant vs. Store Bought  | Soil Quality, Precipitation  | # of Farmers Markets  | Public Transportation  |
| Experiential  | Consistency, Convenience, Expertise  | Year-Round Availability  | Electricity Price | # of Libraries, Access to High-Speed Internet  | # of Community Gardens  | # of Grocery Stores (proximity)  |

We chose Activation Levers within Product (the actual vegetable), Price, Place, People, and Proximity. Once these Levers and Metrics were ideated, we set about finding the available data. Particular emphasis was placed on data sources that were scalable, so we focused on .gov sources when available. 

Because of data limitations, both due to Datathon hours limitations and lack of public data sources, we revised our model to the following:

## Structural Equation Model v2

| Key Category  | Concept       | Place Levers  | People Levers | 
| ------------- | ------------- | ------------- | ------------- | 
| Interest      | Sustainability, Community, Education  | Number of Libraries per Capita  | Number of "Ohio Proud" Farmers Markets per Capita, Library Card Holders per Capita  | 
| Need     | Positive Mental Health, Fight Against Hunger  | # Unserved Sq. Miles for Broadband | Population at Poverty Level per Capita, SNAP Households per Capita, Prescription Benzodiazepine Doses Dispensed per Capita |
| Opportunity    | Climate Change, Digital Connectivity, Environment, Open Space  | Annual Precipitation, Annual Air Quality Index, Avg. Electricity Rates, Annual UV Index, Available Vacant Land | | 

All Levers were gathered by county for the state of Ohio.

## Data Sources

- Population by County ([2020 Census](https://www.census.gov/programs-surveys/decennial-census/decade/2020/2020-census-main.html))
- County Square Miles by County ([2020 Census](https://www.census.gov/programs-surveys/decennial-census/decade/2020/2020-census-main.html))
- Number of Households by County ([2020 Census](https://www.census.gov/programs-surveys/decennial-census/decade/2020/2020-census-main.html))
- SNAP Households by County ([2020 Census](https://www.google.com/url?q=https://data.census.gov/table/ACSST1Y2022.S2201?t%3DIncome%2Band%2BPoverty:SNAP/Food%2BStamps%26g%3D040XX00US39$0500000&sa=D&source=editors&ust=1699192183976336&usg=AOvVaw1YFlfxb-rm3O-PVWJXJewp))
- Population at Poverty Level ([2020 Census](https://www.census.gov/programs-surveys/decennial-census/decade/2020/2020-census-main.html))
- Annual Precipitation ([2022 Rainfall](https://www.google.com/url?q=https://www.ncei.noaa.gov/access/monitoring/climate-at-a-glance/county/mapping/33/pcp/202301/12/value&sa=D&source=editors&ust=1699192183977390&usg=AOvVaw2bd_gkzJHsM_AOdoKNFxGR))
- Number of Library Card Holders per Capita and Number of Libraries per County ([2022 Public Library Statistics](https://www.google.com/url?q=https://library.ohio.gov/libraries/ohio-public-library-statistics/stats-and-reports&sa=D&source=editors&ust=1699192183977718&usg=AOvVaw0zhbHAqsTdIuqmzBC_Pu8s))
- Annual Air Quality Index ([2022 Air Quality Action Days](https://www.google.com/url?q=https://www.epa.gov/ghgreporting/data-sets&sa=D&source=editors&ust=1699192183978247&usg=AOvVaw0TPXh1ID0m_g2elWZjh5hJ))
- Broadband Service per County ([Broadband Ohio](https://www.google.com/url?q=https://broadband.ohio.gov/view-maps/ohios-broadband-availability-gaps&sa=D&source=editors&ust=1699192183978709&usg=AOvVaw2ahuwM8pyUK1jE9PkMnQWe))
- Electricity Rates ([Investor Owned Utilities](https://www.google.com/url?q=https://catalog.data.gov/dataset/u-s-electric-utility-companies-and-rates-look-up-by-zipcode-2020&sa=D&source=editors&ust=1699192183979613&usg=AOvVaw2LqbIb9Api9sVVfAgpJ-wL))
- Annual UV Index ([Cancer.gov](https://www.google.com/url?q=https://gis.cancer.gov/tools/uv-exposure/&sa=D&source=editors&ust=1699192183979011&usg=AOvVaw1GVHDAf32bbh6ZBPN7cEN7))
- Approximate Usable Yard Space ([Avg. Ohio Lot Size - Median Home Size per County in Sq. Ft](https://www.google.com/url?q=https://www.realtor.com/research/data/&sa=D&source=editors&ust=1699192183981195&usg=AOvVaw1x4zmht95GSw5nKVdgKoOw))
- Prescription Benzodiazepine Doses Dispensed per Capita ([2021](https://www.google.com/url?q=https://mha.ohio.gov/static/ResearchandData/DashboardsAndMaps/Maps/BenzoDosesperCapita2021.pdf&sa=D&source=editors&ust=1699192183980888&usg=AOvVaw0H9JekFH_d-M_a5czTtzFu))
- Number of "Ohio Proud" Farmers Markets ([2023 Results](https://www.google.com/url?q=http://ohioproud.org/farm-markets-all/farmers-market-search/find-a-farmers-market/%23!directory/map&sa=D&source=editors&ust=1699192183980241&usg=AOvVaw3Fb2vYnpGiK3opAdcQQa4K))


# Analysis

We performed two analyses with the available data to best construct our model: a Factor Analysis in Jupyter Notebook (python) and a Regression Analysis to determine coefficient weighting in R (programming language). For both, we used a cleaned dataset which removed smaller counties where poverty data was unavailable. 

## Exploratory Factor Analysis[^2]

We performed an Exploratory Factor Analysis in order to understand the underlying trends within our data. In order to do that, we compared our data and grouped them based on correlation. The result was two factor groupings: Socioeconomic Status which included metrics such as SNAP usage, poverty levels, depression, and to a lesser extent available yard space; and Digital and Education Connectivity which included metrics such as access to broadband internet and number of library card holders.

![Factor Analysis Plot](https://github.com/scatterplotsandtea/un_datathon_2023/assets/112765834/5a455f5e-e9f4-46c3-bf9e-2d7c2fcb7a2f)


## Regression Analysis

For our Regression Analysis, we focused on Positive Mental Health to drive our model weighting. Negative correlations decreased prescriptions per capita scores while positive correlations increased prescriptions per capita scores by county. In our scenario, our goal was to decrease prescriptions per capita. Looking at an example from the numbers below, our data indicated that the higher the number of Farmers Markets in a county, the less prescription Benzodiazepine doses would be issued for that county. These coefficients should be used to forecast prescription doses should the metrics listed change.

| Metric | Correlation | Coefficient |
| ------------- | ------------- | ------------- | 
| Farmers Markets | Negative | 39090.59 |
| Available Vacant Land | Negative | 36648.66 |
| UV Index | Positive | .01 |
| Electricity Rates | Negative | 30.27 |
| Broadband Service | Positive | .01 |
| Air Quality Index | Negative | .01 |
| Library Count by County | Negative | 14097.76 |
| Library Card Holders per Capita | Negative | .04 |
| Precipitation | Positive | .01 |
| Poverty per Capita | Negative | 27.38 |
| SNAP per Capita | Positive | 97.34 |

# Composite Score[^3]

Once our analyses were complete, we created a Composite Score for Opportunity. We calculated the average and then placed counties in ranked order. In addition, we looked at each county based on the two factors we identified earlier to determine where investment was most likely to make an impact.

![Key Opportunity Factors by County](https://github.com/scatterplotsandtea/un_datathon_2023/assets/112765834/c2a11d33-f39d-494f-b457-99ac49f898a3)

![Key Opportunity Counties](https://github.com/scatterplotsandtea/un_datathon_2023/assets/112765834/5329ba03-f4f9-49b3-99d4-c78adc78c321)

[^1]: We used the basic modeling technique as described [here](https://hbr.org/2023/05/how-brand-building-and-performance-marketing-can-work-together)
[^2]: We used the basic coding performed [here](https://medium.com/gitconnected/factor-analysis-for-marketing-with-python-f51fbf460c30)
[^3]: We used the coding [here](https://medium.com/analytics-vidhya/the-factor-analysis-for-constructing-a-composite-index-2496686fc54c) as a foundation

