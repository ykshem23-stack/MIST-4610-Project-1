# Group 2 MIST 4610 Project 1

## Team Members
- Yesha Ghandi
- Bradley Guy
- Ivan Jaiwant
- Yusuf Kshem
## Data Model
Our model is based on the structure of global regions and the countries that belong to them. The Region entity represents large geographic areas across the world, containing attributes such as regionID, regionName, areaSqKm, climateZone, and description. Each region contains many countries, which is why there is a one-to-many relationship between the Region and Country entities.

The Country table serves as the central component of the model. It includes each country’s countryID, countryName, countryAbbreviation, population, and region_regionID (a foreign key referencing Region). Because countries can contain multiple free-associated states, there is a one-to-many relationship between the Country and Free_Associated_State entities. Each country also has multiple cities, represented through a one-to-many relationship between the Country and City entities. The City table includes attributes such as cityCode, cityName, isCapital, and isLargestCity, identifying whether a city is the capital or the largest in its country.

Each country in the model contains a variety of national-level data that is stored across multiple connected tables. These include Demographics, Labor_Force, Economy, Education, Health, and Environment, all of which have a one-to-one relationship with the Country table. The Demographics table captures gender distribution statistics such as malePercentage and femalePercentage within the population. The Labor_Force table provides information about the totalLaborForce and unemploymentRate for each country. The Economy table stores national economic indicators, including GDP, minWageUSD, CPI, CPIChange, taxRevenue, and totalTaxRate. The Education table records enrollment rates for grossPrimaryEducEnroll and grossTertiaryEducEnroll, while the Health table stores key measures such as infantMortality, maternalMortality, lifeExpectancy, and birthRate. Lastly, the Environment table holds information related to environmental conditions, such as agriculturalLand, forestedArea, co2Emissions, landAreaSqKm, and densityPerSqrKm.

Countries are also linked to both the Primary_Language and Currency entities through associative tables to capture many-to-many relationships. The Primary_Language_has_Country table allows multiple countries to share the same language while also allowing a single country to have several official languages. Similarly, the Currency_has_Country table connects countries to the currencies they use, since some nations share the same currency and others recognize more than one.

Overall, this model provides a complete and relational view of global data, connecting regions, countries, and their key social, economic, environmental, and cultural attributes. It enables meaningful exploration of how national characteristics relate to one another across regions of the world.
![IMAGE](https://github.com/user-attachments/assets/35471669-c92e-40db-8c32-323c0f5fa82c)

## Data Dictionary
<img width="536" height="234" alt="Table_region" src="https://github.com/user-attachments/assets/5d47992f-7719-450e-b5cf-c5bba8599f73" />

<img width="542" height="245" alt="table_country" src="https://github.com/user-attachments/assets/0ca62732-9b52-4c55-afc5-dacb2280e220" />

<img width="538" height="206" alt="table_city" src="https://github.com/user-attachments/assets/7186db86-5ccf-4990-8321-7fe0b65a20b4" />

<img width="537" height="179" alt="table_demo" src="https://github.com/user-attachments/assets/f48bbd2c-0fa2-46ca-9353-4d676ed6e8a8" />

<img width="541" height="170" alt="table_labor" src="https://github.com/user-attachments/assets/21e048d6-7b58-4a1b-b1a7-98ffa17189d3" />

<img width="536" height="283" alt="table_econ" src="https://github.com/user-attachments/assets/9b13dad8-b3b6-4821-a9dd-80f70cacaa60" />

<img width="539" height="185" alt="table_educ" src="https://github.com/user-attachments/assets/c4353fd1-212b-4cd5-87fb-a3f78f8889f2" />

<img width="539" height="283" alt="table_health" src="https://github.com/user-attachments/assets/85d3e96e-970a-43a5-98ae-209fd2fd1a60" />

<img width="523" height="260" alt="table_env" src="https://github.com/user-attachments/assets/19782141-b31e-4cff-aff6-c79666fc2a12" />

<img width="524" height="189" alt="table_primary_language" src="https://github.com/user-attachments/assets/f19e21cb-6f56-4349-83cb-e37cb0c3e225" />

<img width="524" height="188" alt="table_currency" src="https://github.com/user-attachments/assets/f78cd932-7fb8-467f-9e9c-1a4f5a4a980d" />

<img width="521" height="142" alt="table_currency_has_country" src="https://github.com/user-attachments/assets/012e24e9-2ccb-42bb-a5d1-c7f49603c5e8" />


## Queries
<img width="668.8" height="291.5" alt="query_feature" src="https://github.com/user-attachments/assets/64bb060a-b395-4503-83b4-f8cf872aa03e" />

1.  Query 1 lists the region name, the inflation category (High or Low), the number of countries in each category, and CPI statistics.
Query 1 helps analysts see which regions are experiencing high or low inflation relative to the global average. This information could guide economic policy decisions or investment strategies, highlighting regions where inflation is most severe or stable.

<img width="467.1" height="467.1" alt="query1" src="https://github.com/user-attachments/assets/be256fcc-18db-4ce9-beec-9d8acbcec2a2" />
<img width="488.7" height="297" alt="query1_result" src="https://github.com/user-attachments/assets/547b9668-01f9-48da-8177-0dc105f05533" />

2.  Query 2 lists the region name, education tier (Low, Mixed, High), the number of countries in each tier, average minimum wage, and average primary and tertiary enrollment. 

Query 2 provides insight into the relationship between educational investment and economic outcomes by region. By identifying whether higher education levels correlate with higher wages, policymakers or international organizations can better target initiatives to improve economic performance.

<img width="391" height="349" alt="query2" src="https://github.com/user-attachments/assets/78913cd2-fa36-47ff-a73c-afdcc6fef06e" />
<img width="508" height="297" alt="query2_result" src="https://github.com/user-attachments/assets/78c33619-f912-4a5a-a160-b4f9cc627cf7" />

3.  Query 3 lists each country, its GDP, carbon emissions, and GDP per ton of carbon emitted. 

Query 3 evaluates economic efficiency in relation to environmental impact. This analysis could inform sustainability programs or investment in green technologies by showing which countries produce higher GDP per unit of pollution.

<img width="520.4" height="436" alt="query 3" src="https://github.com/user-attachments/assets/7d517ea3-7cfc-4635-a390-b51e3f245a1d" />
<img width="338" height="294" alt="query3_result" src="https://github.com/user-attachments/assets/f0d6ce2f-16d8-46f5-b964-dc532cfbda75" />

4.  Query 4 lists each country, its GDP, GDP per tax percentage, and a tax category (High or Low). 

Query 4 examines whether higher taxes suppress economic growth. This could influence fiscal policy decisions or corporate investment strategies by highlighting countries where tax burden corresponds with economic performance.

<img width="374.4" height="284.4" alt="query4" src="https://github.com/user-attachments/assets/72d8cd9b-3a24-4b10-b40d-0ed05b7f3312" />
<img width="384" height="295" alt="query4_result" src="https://github.com/user-attachments/assets/a249883d-448e-4b87-961a-c5aa252774c0" />

5.  Query 5 lists each country, its population, GDP, and GDP per capita. 

Query 5 measures economic output per person, helping analysts compare living standards or evaluate economic efficiency. These insights can support development planning or global market assessments.

<img width="381.88" height="277.05" alt="query5" src="https://github.com/user-attachments/assets/c00a8afe-e83b-4c1c-8096-58c38f437727" />
<img width="299" height="296" alt="query5_result" src="https://github.com/user-attachments/assets/0edf7e9a-209a-499e-93c7-135d86399c4d" />

6.  Query 6 lists each country, its sustainability score, normalized score within its region, and rank in the region. 

Query 6 identifies the top environmentally sustainable countries per region. The results could guide ecological initiatives, international aid programs, or investment in countries with strong environmental management practices. 

<img width="630.5" height="410.8" alt="query6" src="https://github.com/user-attachments/assets/dddbdcb6-34b1-4869-84ef-5ff8ff4f0583" />
<img width="377" height="295" alt="query6_result" src="https://github.com/user-attachments/assets/def90f3c-7e60-453b-a451-9f1ddc4f6298" />

7.  Query 7 lists each country, GDP, GDP per population density, and a density category (Above or Below Average). 

Query 7 explores how population concentration affects economic output. This information could assist in urban planning, infrastructure development, or population management policies by showing where high density correlates with economic efficiency. 

<img width="377.52" height="291.72" alt="query7" src="https://github.com/user-attachments/assets/c9b8735e-828d-4ece-a97d-dae3462befb7" />
<img width="475" height="293" alt="query7_result" src="https://github.com/user-attachments/assets/b37f438e-288f-4f0a-b54c-b9fdaa5321ad" />

8.  Query 8 lists each currency, and the average GDP of countries using that currency. 

Query 8 highlights which currencies are associated with the highest economic output. This can inform investment decisions, currency risk analysis, and international economic comparisons. 

<img width="526" height="222" alt="query8" src="https://github.com/user-attachments/assets/74ecf6e5-5904-4900-8c87-42544fca1d8f" />
<img width="394" height="132" alt="query8_result" src="https://github.com/user-attachments/assets/0f9305ee-bb00-4e4e-b2b6-e68f5e42acbb" />

9.  Query 9 lists each country, its infant mortality, and its region, focusing on countries with infant mortality above the regional average whose languages do not contain the “an” pattern. 

Query 9 highlights countries with poor health outcomes that deviate from typical linguistic patterns. These insights could help direct targeted health interventions or regional public health programs to areas with critical needs. 

<img width="538.5" height="451.5" alt="query9" src="https://github.com/user-attachments/assets/32d9d80d-8410-415d-b7b1-9f90cefb951d" />
<img width="339" height="445.5" alt="query9_result" src="https://github.com/user-attachments/assets/27d468bb-8991-4ab3-b91e-a760fa4e6ed0" />

10.  Query 10 lists each region, its average infant mortality, and average maternal mortality. 

Query 10 identifies regions with the worst health outcomes. This information could guide the allocation of healthcare resources or international aid, prioritizing regions with high mortality rates for intervention programs.  

<img width="484" height="260" alt="query10" src="https://github.com/user-attachments/assets/d08a00b2-2fc0-4f96-b60b-084ae95ef009" />
<img width="422.4" height="107.2" alt="query10_result" src="https://github.com/user-attachments/assets/8d4bf014-54f5-4e73-9578-6ae11bc4e80d" />




## Database Info
Name of the database: cs_yrk51993

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL Group2_Qx();

Where 'x' refers to the Query number.

