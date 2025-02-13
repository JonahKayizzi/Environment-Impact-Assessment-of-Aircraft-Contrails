# Project Proposal: Enhancing Contrail Prediction Models for Africa

## ABSTRACT

The aviation industry faces growing challenges from rising air travel demand and environmental concerns, particularly the significant radiative forcing (RF) effects of contrails, which are estimated to have three times the climate impact of aviation’s CO₂ emissions. With only 2% of flights accounting for 80% of contrail RF, the need for precise contrail mitigation strategies is pressing. However, existing contrail prediction models suffer from inaccurate humidity measurements, which are crucial for contrail formation and persistence.

This project proposes a comprehensive solution to improve contrail prediction models by introducing new model inputs that account for prevailing environmental conditions in Africa. These inputs include proximity to water bodies (lakes, rivers, oceans), dense forests, and mountainous regions, which significantly influence atmospheric humidity and contrail formation. By integrating these geographical and climatic factors with advanced satellite indices and band information, we aim to enhance the accuracy of contrail prediction models and support sustainable aviation practices in Africa.

## 1.0 INTRODUCTION

The aviation industry faces the dual challenge of meeting rising global demand for air travel while reducing its environmental impact. Over the next two decades, global passenger traffic is expected to grow at an average annual rate of 3.8%, adding 4 billion journeys by 2043. This expansion increases the industry's environmental footprint, which accounts for 4% to 5% of global warming [1]. While CO2 emissions have traditionally been the focus, contrails are now recognized as a significant contributor to aviation-induced climate forcing, with their radiative forcing estimated to be three times greater than aviation's CO2 emissions [1]. Studies indicate that just 2% of flights are responsible for 80% of contrail energy forcing [2], with projections suggesting that contrail radiative forcing could triple by 2050 [4].

Regulatory responses include ICAO's M1-AMET module of the Global Air Navigation Plan (GANP), which aims to enhance flight planning through accurate meteorological data, and the EU's mandate for 70% sustainable aviation fuels by 2050 [5]. However, contrail mitigation requires real-time prediction and avoidance strategies. Current contrail prediction models lack the precision needed to measure atmospheric conditions conducive to contrail formation, especially in Ice Supersaturated Regions (ISSR) [6][7].

This project aims to address the prevailing problem of inaccurate humidity measurements in contrail prediction models by improving their input data. By integrating new model inputs such as proximity to water bodies, dense forests, and mountains, we aim to enhance the accuracy of contrail prediction models and support sustainable aviation practices in Africa.

## 2.0 BACKGROUND

Contrails, or condensation trails, are line-shaped clouds formed by aircraft engine exhaust when it mixes with cold, humid air at high altitudes. These contrails can persist and evolve into contrail cirrus clouds, contributing significantly to the radiative forcing of the Earth's atmosphere. The impact of contrails on climate change has become a critical area of research, as their radiative forcing is estimated to be three times greater than that of aviation's CO₂ emissions. Therefore, accurately predicting and mitigating contrail formation is essential for reducing the aviation industry's environmental footprint.

Contrail formation is highly dependent on atmospheric conditions, particularly humidity and temperature. However, existing prediction models often suffer from inaccurate humidity measurements, leading to suboptimal contrail mitigation strategies. Given the complexity of atmospheric processes, it is crucial to integrate additional environmental factors, such as proximity to water bodies, dense forests, and mountains, which significantly influence atmospheric humidity and contrail formation.

## 3.0 PROBLEM STATEMENT

Accurate prediction of contrail formation is essential for mitigating their environmental impact. However, current contrail prediction models face significant challenges due to inaccurate humidity measurements. Humidity is a critical factor in contrail formation and persistence, and inaccuracies in its measurement can lead to ineffective contrail mitigation strategies. The prevailing problem is the lack of precision in measuring atmospheric conditions conducive to contrail formation, particularly in Ice Supersaturated Regions (ISSR).

This project aims to address this issue by improving the input data for contrail prediction models. By integrating new model inputs, such as proximity to water bodies, dense forests, and mountains, we seek to enhance the accuracy of contrail prediction models. This will enable more effective contrail mitigation strategies, reduce the aviation industry's environmental impact, and support sustainable aviation practices in Africa.

## 4.0 RESEARCH QUESTIONS

1. How can the integration of proximity to water bodies, dense forests, and mountains improve the accuracy of contrail prediction models?
2. What are the specific environmental conditions in Africa that significantly influence atmospheric humidity and contrail formation?
3. How can advanced satellite indices and band information be utilized to enhance the precision of humidity measurements for contrail prediction models?
4. What are the potential benefits of improved contrail prediction models for the aviation industry's environmental impact and operational efficiency in Africa?
5. How can machine learning algorithms be applied to refine contrail prediction models with the new environmental inputs?

## 5.0 LITERATURE REVIEW

### 5.1 Contrail Formation and Persistence

Contrails are line-shaped clouds formed when hot, humid aircraft exhaust mixes with cold ambient air, causing water vapor to condense and freeze. These clouds, though seemingly benign, have a significant and complex climate impact. Atmospheric conditions, particularly temperature and humidity, determine contrail persistence. In low-humidity regions, contrails evaporate quickly, while in high-humidity conditions, they persist and may merge with existing cirrus clouds to form contrail cirrus, amplifying their climate impact [1].

### 5.2 Environmental Impact of Contrails

Recent studies highlight the significant role of contrails in aviation's climate impact. Gryspeerdt et al. (2024) project that contrail cirrus radiative forcing could triple by 2050, driven by increased air traffic and higher altitudes [11]. Similarly, Teoh et al. (2024) found that contrail cirrus radiative forcing is about three times greater than aviation's cumulative CO2 emissions [2]. The environmental impact of contrails depends on factors such as time of day, altitude, and atmospheric conditions. Addressing contrail formation could help mitigate rising operational costs and improve sustainability [4, 8].

### 5.3 Contrail Prediction and Avoidance

Accurate prediction and mitigation of contrail formation are key research areas, with tools like the Schmidt-Appleman Criterion and advanced models such as the Contrail Cirrus Prediction Model (CoCiP) enhancing prediction accuracy [2]. However, the IATA June 2024 report underscores the challenge of limited real-time meteorological data at cruising altitudes for contrail prediction and avoidance [12]. Current contrail prediction models lack the sensitivity needed for accurate humidity measurements, which are critical for predicting contrail formation.

### 5.4 Integrating Environmental Factors for Improved Prediction

Proximity to water bodies, dense forests, and mountains significantly influence atmospheric humidity and contrail formation. Large water bodies and dense forests are key sources of evaporation and transpiration, contributing to local atmospheric humidity. Mountains influence atmospheric pressure and temperature, affecting moisture retention and condensation. By integrating these factors with satellite indices and band information, we can develop more accurate contrail prediction models.

## 6.0 METHODOLOGY

### 6.1 Data Collection

#### 6.1.1 Satellite Data

- Use NDVI and NDWI from satellites like Sentinel-2, Landsat-8, or MODIS.
- Get atmospheric humidity data from ERA5 Reanalysis or NASA’s MERRA-2.

#### 6.1.2 Geospatial Layers

- Proximity to water bodies (download hydrological layers, e.g., from HydroSHEDS).
- Forest cover data from Global Forest Watch or MODIS Vegetation Continuous Fields.
- Digital Elevation Models (DEMs) for mountains (e.g., SRTM or ASTER).

#### 6.1.3 Climatic and Meteorological Data

- Rainfall and temperature patterns from climate datasets (e.g., WorldClim, CHIRPS).

### 6.2 Data Integration

Use GIS software (e.g., QGIS, ArcGIS) or Python for data integration:

- Overlay NDVI, NDWI, proximity to water bodies, forest cover, and elevation.
- Calculate distances to major lakes, rivers, and oceans.
- Identify regions with high NDVI/NDWI, near water bodies, dense forests, and significant elevation.

### 6.3 Statistical or Machine Learning Modeling

Combine all datasets into a statistical model or machine learning framework:

- Use NDVI/NDWI as predictors alongside proximity to water bodies, forest density, elevation, and climatic variables.
- Train models to predict atmospheric humidity using ground-truth humidity data from weather stations.

### 6.4 Validation

Validate results by comparing deduced humidity with meteorological observations. Refine models to account for variables like soil type, land cover, and seasonal variations.

## 7.0 APPLICATION OF THE MODEL FOR CONTRAIL PREDICTION

### 7.1 Advanced Flight Planning with Predictive Environmental Impact Assessment

Create a weather database alongside an aeronautical database within an ATM system for flight planning. Populate the weather database with essential weather parameters required for contrail prediction, retrieved in real-time from cloud-based services. Use a three-dimensional airspace grid to dynamically associate weather parameters with each airspace cell.

### 7.2 Real-time Environmental Impact Awareness for Flight Crew

Provide real-time environmental impact awareness to the flight crew through the onboard Electronic Flight Bag (EFB). The EFB will act as an interface between the flight crew and the environmental impact prediction model, offering updated contrail prediction based on real-time weather parameters. This integration allows the crew to make informed, proactive decisions, requesting adjustments to the flight path to reduce contrail formation and its associated environmental impact.

## 8.0 CONCLUSIONS AND RECOMMENDATIONS

Integrating new model inputs such as proximity to water bodies, dense forests, and mountains with satellite indices and band information can significantly enhance the accuracy of contrail prediction models. By improving the input data, we can better predict contrail formation and support sustainable aviation practices in Africa. Future developments in remote sensing technologies and data processing algorithms could further advance contrail prediction and mitigation efforts.

## BIBLIOGRAPHY

[1] T. Wagner, “10 figures about aviation and the climate,” Bon Pote. Accessed: Oct. 18, 2024. [Online]. Available: https://bonpote.com/en/10-facts-and-figures-about-airplanes-and-the-climate/
[2] R. Teoh et al., “Global aviation contrail climate effects from 2019 to 2021,” Atmospheric Chemistry and Physics, vol. 24, no. 10, pp. 6071–6093, May 2024, doi: 10.5194/acp-24-6071-2024.
[3] J. Prisco, “Contrails are a problem for aviation – but there could be an easy solution,” CNN. Accessed: Oct. 22, 2024. [Online]. Available: https://www.cnn.com/travel/article/contrails-aviation-climate-change-satavia-scn-spc-intl/index.html
[4] D. K. Singh, S. Sanyal, and D. J. Wuebbles, “Understanding the role of contrails and contrail cirrus in climate change: a global perspective,” Atmospheric Chemistry and Physics, vol. 24, no. 16, pp. 9219–9262, Aug. 2024, doi: 10.5194/acp-24-9219-2024.
[5] “ReFuelEU Aviation - European Commission.” Accessed: Oct. 14, 2024. [Online]. Available: https://transport.ec.europa.eu/transport-modes/air/environment/refueleu-aviation_en
[6] “IATA - More Data Needed to Understand Contrails, their Climate Effect & Develop Mitigation.” Accessed: Nov. 06, 2024. [Online]. Available: https://www.iata.org/en/pressroom/2024-releases/2024-04-30-01/
[7] B. Wang, B. Han, K. Wang, and S. Cao, “Air vehicle humidity sensor based on PVA film humidity sensing principle,” APL Materials, vol. 12, no. 7, p. 071116, Jul. 2024, doi: 10.1063/5.0213766.
[8] S. Atalay, T. Izgi, V. S. Kolat, S. Erdemoglu, and O. O. Inan, “Magnetoelastic Humidity Sensors with TiO2 Nanotube Sensing Layers,” Sensors, vol. 20, no. 2, Art. no. 2, Jan. 2020, doi: 10.3390/s20020425.
[9] Z. Wang et al., “Machine learning for improvement of upper tropospheric relative humidity in ERA5 weather model data,” EGUsphere, pp. 1–28, Jul. 2024, doi: 10.5194/egusphere-2024-2012.
[10] “Lufthansa Group introduces Environmental Cost Surcharge,” Lufthansa Group introduces Environmental Cost Surcharge. Accessed: Oct. 12, 2024. [Online]. Available: https://newsroom.lufthansagroup.com/en/lufthansa-group-introduces--environmental-cost-surcharge/
[11] G. Horner and E. Gryspeerdt, “How does the lifetime of detrained cirrus impact the high cloud radiative effect in the tropics?,” EGUsphere, pp. 1–22, Apr. 2024, doi: 10.5194/egusphere-2024-1090.
[12] “IATA - Global Outlook for Air Transport Deep Change, June 2024 Report.” Accessed: Nov. 06, 2024. [Online]. Available: https://www.iata.org/en/iata-repository/publications/economic-reports/global-outlook-for-air-transport-june-2024-report/
[13] “ICAO - 2016–2030 Global Air Navigation Plan.” Accessed: Nov. 11, 2024. [Online]. Available: https://www.iata.org/contentassets/1be2bec28b3d45f9ae7780d6ebea7be9/icao_ganp_doc209750_5ed_en.pdf
[14] Johan Gönczi (2023). Strategies to avoid persistent contrail conditions in aviation Flight planning strategies for mitigating the climate impact of the aviation industry.
[15] “Google & American Airlines’ AI Aviation Contrail Reduction | Sustainability Magazine.” Accessed: Nov. 17, 2024. [Online]. Available: https://sustainabilitymag.com/articles/google-american-airlines-ai-aviation-contrail-reduction
[16] “ATC Clearances and Aircraft Separation.” Accessed: Nov. 17, 2024. [Online]. Available: https://www.faa.gov/air_traffic/publications/atpubs/aim_html/chap4_section_4.html
[17] “Departure Procedures.” Accessed: Nov. 15, 2024. [Online]. Available: https://www.faa.gov/air_traffic/publications/atpubs/aim_html/chap5_section_2.html
[18] “Aircraft Contrail Prediction for Commercial Flights” Accessed: Nov. 15, 2024. [Online]. Available: https://www.diva-portal.org/smash/get/diva2:1698423/FULLTEXT01.pdf
[19] “AMDAR Onboard Software Functional Requirements Specification.” Accessed: Nov. 17, 2024. [Online]. Available: https://library.wmo.int/records/item/51390-amdar-onboard-software-functional-requirements-specification#.XVFuR66WZtQ