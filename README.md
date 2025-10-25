# MIST-4610-Project-1

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
![IMAGE](https://github.com/user-attachments/assets/43e1516f-acd0-4103-a22e-c00376b4a37b)
## Data Dictionary
<img width="536" height="234" alt="Table_region" src="https://github.com/user-attachments/assets/1c6ee8e8-baf6-42e7-8101-491418bf9e94" />

<img width="542" height="280" alt="table_country" src="https://github.com/user-attachments/assets/5ff8c987-65ce-4278-a936-85a695fcd8ee" />

<img width="538" height="230" alt="table_city" src="https://github.com/user-attachments/assets/9bb71241-3b79-4a53-81a8-7de3896e48cf" />

<img width="539" height="164" alt="table_demo" src="https://github.com/user-attachments/assets/051f49a0-fe3e-42c9-9e80-a6a5c87b4a29" />

<img width="537" height="212" alt="table_labor" src="https://github.com/user-attachments/assets/a95d6b5e-7590-40ab-ad16-93511c27dc74" />

<img width="540" height="284" alt="table_econ" src="https://github.com/user-attachments/assets/84256fd1-137b-4720-8745-5924f27dd31e" />

<img width="539" height="185" alt="table_educ" src="https://github.com/user-attachments/assets/a6408cca-6995-4110-b506-c17e3a9bce42" />

<img width="539" height="283" alt="table_health" src="https://github.com/user-attachments/assets/de4faf1a-5e89-4ba7-9aba-912b33159556" />

<img width="523" height="260" alt="table_env" src="https://github.com/user-attachments/assets/697f9bec-90de-42a9-9e5b-68e79fde26f6" />

<img width="492" height="182" alt="table_primary language" src="https://github.com/user-attachments/assets/bd23c464-b86f-4961-a0c9-d172e60671b7" />

<img width="525" height="188" alt="table_currency" src="https://github.com/user-attachments/assets/ecce634e-5251-459a-bd61-9e3628eb3920" />

<img width="528" height="191" alt="table_currency_has_country" src="https://github.com/user-attachments/assets/2cb1259e-a767-467a-bb66-36587b467479" />

## Queries
<img width="668.8" height="291.5" alt="query_feature" src="https://github.com/user-attachments/assets/64bb060a-b395-4503-83b4-f8cf872aa03e" />
1.  Query 1 lists the region name, the inflation category (High or Low), the number of countries in each category, and CPI statistics.
Query 1 helps analysts see which regions are experiencing high or low inflation relative to the global average. This information could guide economic policy decisions or investment strategies, highlighting regions where inflation is most severe or stable.







## Database Info

