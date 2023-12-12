---
date: "2023-12-12T00:00:00Z"
external_link: ""
image:
  focal_point: Smart
summary: First assignment for Data analysis for sustainable development 2023. 
tags:
- Food
- Soy
title: Soy flows in the EU
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""
---

Agriculture has a large impact on the environment (SOURCE). Biodiversity loss, land-use change, eutrification, and climate change, are all linked to agriculture and put increasing pressure on society (SOURCE). Soy, or soya, is one of the most widely produced and used crop in the world (SOURCE). The use of soy, however, is among other things often linked to deforestation in rainforests, and is therefore often not sustainable. To get a better overview of the use of soy in the EU, data from Eurostat and the FAO has been analyzed using Python. This report contains a usage analysis, and a results section which includes some of the basic steps that have been taken for this analysis. 

__Usage analysis__

The data for this report is from Eurostat, and FAO. In total three datasets have been used. Firstly, detailed trade in goods data has been used to quantify the imports and exports of soy to and from the EU (Eurostat, 2023, 1). This data contains the amounts of soy and the source/target of the imports/exports, split up over three different types. Secondly, data on the usage of Soy has been extracted from the FAO database. For this the food balances from 2010 onwards have been used (FAO, 2023). This dataset specifies the amount of soy that is used in various applications, split up over the three types of soy used. The dataset also contains data on the imports and exports of soy, and the own production, however does not specify where the soy is from. Lastly, a dataset on the own production of soy within the EU was used. This again is from the Eurostat database, but this time on the agricultural production in EU standard humidity (Eurostat, 2023, 2). The data splits up the production of soybeans by EU country. 

Since the datasets contain only one variable of interest (weight of the soy product), the usage analysis is qualitative. A visualisation of the data is shown in the results section, since this is the main outcome of the data analysis. Firstly, the Eurostat database. Eurostat uses a standardised approach for generating its statistics called the European Statistical System (ESS) (Eurostat, 2023, 3). In this system peer reviews are issued to make sure that statistical measures are applied consistently throughout the member countries. This makes Eurostat a credible source of data. The detailed trade in goods data is widely used in literature, as a quick Google Sholar search shows (for example: Havlik et al. (2009), Thissen et al. (2019), Martinez-Zarzoso et al. (2015)). The agricultural production dataset is also widely used in literature to quantify the agricultural production in the EU (For example: Reidsma et al. (2009), and Einarsson (2021)). 

Both datasets contain some missing data. For the agricultural production the missing data are mainly in countries where other years there is no production of soybeans (The Netherlands, and Lithuania). It is therefore assumed that in the years with missing values there is also no production. For Germany there is some production from 2016 onwards, and before that there are missing values. The production in Germany, however, is very low compared to other producing countries and therefore assuming no production for the missing values does not have a big impact on the results of the analysis. For the import and export database, the missing values are a bit of a bigger problem. The missing values have are present throughout the dataset, and there are patterns to this, where some countries have completely missing data, or missing data for a whole product type. However, as some countries do not produce/import soy, or do not produce/import a certain soy product, the missing values might sometimes indicate that there is no soy trade with this country. Given that the Eurstat database is widely used and has high data gathering standards, it is therefore chosen to just represent the missing value as a value of zero. The import and export of soy is later in the assignment compared to the values used by the FAO and these are similar, indicating that there are no big issues with the data, or there is not an easy remedy for this. 

FAOSTAT, the statistics body of the FAO, also uses a standardized method for the gathering and reporting of data (FAOSTAT, 2023). The food balances dataset is also a widely used dataset for the analysis of food systems (For example: Sheehy et al. (2019), and Ridoutt et al. (2017)). In this dataset there is a limited amount of missing data, and the data that is missing is mainly present because a certain soy product cannot be used for that purpose (for example the use of soybean meal for planting new soy). The main exeption to this is the consumption of soy products by tourists in the EU. The impact of this, however, is probably small and therefore again it is chosen to regards missing values as zero values. 

__Results__

In the analysis, three types of soy products have been identified. Firstly, whole or only slightly processed soybeans, which are shown as soybeans. Secondly, soybean oil which is an oil made from pressing soybeans. This is shown as soybean oil, soy-oil or just oil. Lastly, soybean meal which is what is left after processing soybeans to extract soybean-oil. This is shown as soybean meal, soymeal or just meal. The distinction between these three types is both made by the EU and FAO. 

To present all the information that is available in the datasets in a comprehensive way, two dash apps were made (See figure 1 and 4). Figure 1 shows the imports of different soy types to the EU, the exports from the EU, and the own production of soybeans within the EU. The map shows that most soy is imported from South-America, mainly Brazil and Argentina. This is confirmed by the bar chart which shows the seven largest sources of soy for the EU. For almost all years Brazil, Argentina, and the US are the largest producing countries. Figure 2 further shows the total imports over time and shows that the rest of the world combined is usually as large as the imports from the US, and around a third to a halve the imports from Brazil. This shows how large the imports from the top three countries are. 

{{< rawhtml >}}
<iframe src="https://soy-trade-europe.onrender.com" width=100% height=760"></iframe>
{{< /rawhtml >}}
<span style="font-size: smaller;">*Figure 1: soy trade with the EU, and own production of soy in the EU. Different soy products can be selected in the dropdown menu, and a different flow type can be selected. The slider below the graph can be used to change the year. The results can either be presented on a map or in a bar chart. __It can take a while for the figure to load__. [Click here to go to larger representation  of the graph](https://soy-trade-europe.onrender.com)*</span> 

For both soybean meal and whole soybeans, the results are comparable. Interestingly, when looking at the EU imports of soy oil the picture changes. The EU imports most of it's soy oil from the United Kingdom, followed by other European countries. There are, however, two big limitations in the data that might influence this result. Firstly, the import data are direct imports and do not specify the original source of the soy. For example, Norway sometimes is one of the seven largest exporters of soy to the EU whereas they do not have any own production of soy. They have to have sourced their soy somewhere else, which is not shown in the figures here. Secondly, soybean oil is a processed product and therefore the origin of the oil does not have to be the same as the origin of the soybean. The information on this is not presented in the current graphs, and could hinder the analysis of soy use in the EU as it might underrepresent the import dependency on only a select group of countries, which is already large as shown in figure 2. 

{{< rawhtml >}}
<iframe src="tot_imports.html" width=100% height=500"></iframe>
{{< /rawhtml >}}
<span style="font-size: smaller;">*Figure 2: Top 3 countries for total soy import to the EU. Other represents the total imports from other countries in Europe*</span> 

A last important insight from figure 1 relates to the own production of soy. Within the EU most soy is produced by Italy, followed by mainly eastern European countries and in more recent years France. Many Northern-European countries have no soy production, which is logical given that soy is traditionally cultivated in warmer climates. Although the production in the whole of the EU has gone up (figure 3), the production of soy is much smaller than the imports (around 3 Mtonnes own production, compared to 40 Mtonnes of total soy products being imported). 

{{< rawhtml >}}
<iframe src="production_tot_bar.png" width=100% height=500"></iframe>
{{< /rawhtml >}}
<span style="font-size: smaller;">*Figure 3: soybean production in the EU*</span> 

The last part of the analysis relates to the usage of soy in the EU. This is shown in a Sankey diagram, which combines both the flows of soy to the EU, as well as where these flows are used (Figure 4). Figure 4 is another dash app where different years can be selected in the dropdown menu, and a distinction can be made between showing just the total imports, or the imports split up over the origin. The figures without the source of the soy are solely based on the food balances of the FAO, whereas the others include the Eurostat data from earlier. To make the sankey diagrams a template from datacamp has been used, and the data has therefore been transformed to fit that format. This can all be seen in the python file as well as all the other steps taken in the data analysis. 

The Sankey diagrams provide information on the use of the different types of soy. It can be seen that animal feed is the largest 

{{< rawhtml >}}
<iframe src="https://soy-balance-eu.onrender.com" width=100% height=900"></iframe>
{{< /rawhtml >}}
<span style="font-size: smaller;">*Sankey diagram for the flows of soy in the EU. __It can take a while for the figure to load__. [Click here to go to larger representation  of the graph](https://soy-balance-eu.onrender.com)*</span> 



__References__

Einarsson, R., Sanz-Cobena, A., Aguilera, E., Billen, G., Garnier, J., van Grinsven, H. J., & Lassaletta, L. (2021). Crop production and nitrogen use in European cropland and grassland 1961–2019. Scientific Data, 8(1), 288.

Eurostat (2023, 1). EU trade since 1999 by SITC (ds-018995). Retrieved from: https://ec.europa.eu/eurostat/databrowser/product/view/ds-018995

Eurostat (2023, 2). Crop production in EU standard humidity (apro_cpsh1). Retrieved from: https://ec.europa.eu/eurostat/databrowser/view/apro_cpsh1/default/table?lang=en

Eurostat (2023, 3). Quality, Peer Reviews. Retrieved from: https://ec.europa.eu/eurostat/web/quality/peer-reviews

FAO (2023). Food Balances (2010-). Retrieved from: https://www.fao.org/faostat/en/#data/FBS

FAOSTAT (2023). Methods and standards, Retrieved from: https://www.fao.org/statistics/standards/agriculture/en#navbarNavWebsite

Havlik, P., Pindyuk, O., & Stöllinger, R. (2009). Trade in Goods and Services between the EU and the BRICs (No. 357). wiiw Research Report.

Martinez-Zarzoso, I., Voicu, A. M., & Vidovic, M. (2015). Central East European Countries’ accession into the European Union: role of extensive margin for trade in intermediate and final goods. Empirica, 42, 825-844.

Reidsma, P., Ewert, F., Boogaard, H., & van Diepen, K. (2009). Regional crop modelling in Europe: the impact of climatic conditions and farm characteristics on maize yields. Agricultural Systems, 100(1-3), 51-60.

Ridoutt, B., Baird, D., Bastiaans, K., Darnell, R., Hendrie, G., Riley, M., ... & Keating, B. (2017). Australia’s nutritional food balance: Situation, outlook and policy implications. Food security, 9(2), 211-226.

Sheehy, T., Carey, E., Sharma, S., & Biadgilign, S. (2019). Trends in energy and nutrient supply in Ethiopia: a perspective from FAO food balance sheets. Nutrition journal, 18, 1-12.

Thissen, M., Ivanova, O., Mandras, G., & Husby, T. (2019). European NUTS 2 regions: construction of interregional trade-linked Supply and Use tables with consistent transport flows (No. 01/2019). JRC Working Papers on Territorial Modelling and Analysis.
