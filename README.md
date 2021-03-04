# ☠️ 🚢 Crime at Sea: A Global Database of Maritime Pirate Attacks (1993 - 2020)

This dataset contains information from more than 7,500 maritime pirate attacks that took place between January 1993 and December 2020, as well as country indicator data for the same time period. The pirate attack data was collected from the International Maritime Bureau (IMB), tidied, and augmented with geospatial data. The country indicator data was sourced from a variety of sources, notably The World Bank. The data is contained in Comma Separated Value (CSV) files. The reuse potential includes its use by anti-piracy organisations and researchers, as well as commercial businesses, in the understanding and prevention of maritime piracy. 

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by/4.0/).

![Pirate Attacks in East Africa 1993 - 2020.](img/east_africa_plot.png?raw=true)

## Contents

* `README.md` this file.
* `dataset/`
    * [csv](data/csv) The dataset in csv format.
* `img/` example visualizations and associated imagery.
* `LICENSE` CC BY 4.0.

## Dataset schema

The dataset contains piracy attack data and historical country indicators for 1993 until the end of 2020.

![The database schema.](img/dataset_schema.png?raw=true)

## Codebook

### Pirate Attacks

* **Date [Key]** - Date of Attack. Used as a key with the Country Matrix data frame. 
* **Time** - Time the attack took place, either in UTC or Local Time.
* **Longitude** - Longitude where the attack took place. 
* **Latitude** - Latitude where the attack took place. 
* **Attack Type** - Either NA (Missing), Attempted, Boarding, or Hijacked. 
* **Location Description** - A text description of the location. With attacks taking place at sea, it is not as simple as just naming a city or town. 
* **Nearest Country [Key]** - The country code whose shore is closest to the attack. The resolution is around 1 km, it can be much better depending on how detailed the mapping of the coast is in the vicinity.
* **EEZ Country [Key]** - The Exclusive Economic Zone country code in which the attack took place, if it took place within an EEZ. 
* **Shore Distance** - Distance in kilometres to the shore from the attack location. This is the true geographic distance over the surface of the earth. 
* **Shore Longitude** - The longitude of the closest point on the shore to the attack. 
* **Shore Latitude** - The latitude of the closest point on the shore to the attack. 
* **Attack Description** - The text description of the attack if it exists. 
* **Vessel Name** - The name of the ship which was attacked if it is known.
* **Vessel Type** - The type of vessel attacked if known. 
* **Vessel Status** - The status of the ship at the time it was attacked. Either NA (Missing), Berthed (Tied to a berth), Anchored (anchored at sea or in a harbour), or Steaming (ship underway). 

### Country Indicators

* **Country [Key]** - The country in ISO3 country code format.
* **Corruption Index** - Corruption Perceptions Index.
* **Homicide Rate** - Total Intentional Homicides per 100,000 people.
* **GPD** - Gross Domestic Product (US Dollars).
* **Total Fisheries Per Ton** - Total Fisheries Production (metric tons).
* **Total Military** - Total Number of Armed Forces personnel.
* **Population** - Country Population.
* **Unemployment Rate** - Percentage of the Country Unemployed.
* **Total GR** - Total Government Revenue. An indication of how well the country collects taxes.
* **Industry** - Industrial contribution to total GDP.

### Country Codes

* **Country [Key]** - The country in ISO3 country code format.
* **Region** - The region the country is in.
* **Country Name** - The English country name.

## Authors

P Benden, A Feng, C Howell and GV Dalla Riva.

## Acknowledgements

This dataset would not have been possible without the work of the [International Maritime Bureau (IMB)](https://www.icc-ccs.org/) and [Professor Brandon C. Prins](https://brandonprins.weebly.com/index.html).
