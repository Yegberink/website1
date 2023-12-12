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

FAOSTAT, the statistics body of the FAO, also uses a standardized method for the gathering and reporting of data (FAOSTAT, 2023). The food balances dataset is 


{{< rawhtml >}}
<iframe src="https://soy-trade-europe.onrender.com" width=100% height=900"></iframe>
{{< /rawhtml >}}
<span style="font-size: smaller;">*Soy trade with the EU. [Click here to go to larger representation  of the graph](https://soy-trade-europe.onrender.com)*</span> 


{{< rawhtml >}}
<iframe src="https://soy-balance-eu.onrender.com" width=100% height=900"></iframe>
{{< /rawhtml >}}
<span style="font-size: smaller;">*Sankey diagram for the flows of soy in the EU. [Click here to go to larger representation  of the graph](https://soy-balance-eu.onrender.com)*</span> 

{{< rawhtml >}}
<iframe src="own_production.html" width="100%" height="500px"></iframe>
{{< /rawhtml >}}

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

Thissen, M., Ivanova, O., Mandras, G., & Husby, T. (2019). European NUTS 2 regions: construction of interregional trade-linked Supply and Use tables with consistent transport flows (No. 01/2019). JRC Working Papers on Territorial Modelling and Analysis.
