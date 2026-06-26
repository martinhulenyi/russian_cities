# Russian Cities Spatial Dataset

Spatial data file of Russian cities used in *Russia's Wartime Economy: 
Measuring Regional Inequalities from Outer Space*.

## Description

Data contains spatial information on Russian cities. We obtained the list 
of cities from the [Wikipedia list of Russian cities](https://archive.ph/IjKhf) 
and used them to scrape spatial data from OpenStreetMap using the 
`nominatimlite` R package (OSM data scraped approximately Q3–Q4 2023; 
exact date and package version not recorded).

We do not include the illegally occupied Crimea and Sebastopol, which Russia 
has been claiming as its 84th and 85th federal subjects since 2014, or the 
four regions of Ukraine that it attempted to annex in 2022.

In a small number of cases, we added the term "gorod" (city) to avoid 
retrieving the boundaries of higher-level administrative units rather than 
city-level geometries (Khabarovsk, Irkutsk, Magadan, Tomsk, Vologda, 
Stavropol, Lipetsk, and Onega). For cities sharing the same name but located 
in different regions, we replaced "Russia" with the name of the corresponding 
federal subject in the query (Beryozovsky, Blagoveshchensk, Fokino, Guryevsk, 
Kirov, Kirovsk, Krasnoarmeysk, Krasnoslobodsk, Krasnoznamensk, Mikhaylovsk, 
Mirny, Nikolsk, Ozyorsk, Pavlovsk, Raduzhny, Sovetsk, Troitsk, Zarechny, 
Zelenogorsk, and Zheleznogorsk).

## Geographic Coverage

| Field | Value |
|---|---|
| Country | Russia (Russian Federation) |
| CRS | EPSG:4326 |
| West | 19.842°E (Kaliningrad) |
| East | 177.539°E (Chukotka) |
| South | 42.008°N |
| North | 69.711°N |

## Data Dictionary

**File:** `russian_cities.gpkg`

| Column | Description |
|---|---|
| `city` | City name |
| `subject` | Federal subject in which the city is located |
| `subject_type` | Type of federal subject: Republics; Krais (territories); Oblasts (regions); Federal cities; Autonomous oblast; Autonomous okrugs |
| `district` | Federal district in which the city is located |
| `pop_2011` | Population in 2011 ([source](https://archive.ph/OjT4I)) |
| `border_distance` | Distance to the nearest international border (km, straight-line) |
| `nearest_border` | ISO 3 code of the country with which the nearest border is shared |
| `geom` | Geometry column |

The folder `maps_fed_subjects` contains snapshots of cities by federal subject (83 maps, .png format).

 
## License

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

## Contact

Martin Hulényi — martin.hulenyi@gmail.com
