# data-dynalearn

Processing of the Covid-19 dataset for the "Deep learning of contagion dynamics on complex networks".

## Datasets
Here, we show how the Covid-19 dataset in processed using the raw datasets. Two files are needed and are located in the `raw-dataset` directory of the repository:

### Number of cases
- raw file: `cases-timeseries-20210327.csv`
- processed file: `cases-timeseries.data`
- details:
  - column `provincia_iso` corresponds to the province using the [ISO 3166-2:ES] naming convention;
  - column `fecha` indicates the date in format `YYYY-MM-DD`;
  - column `num_casos` provides the number of daily new cases.
- [original file](https://cnecovid.isciii.es/covid19/resources/casos_tecnica_provincia.csv) downloaded on 2021-03-27.

### Province population sizes
- raw file: `population-data.csv`.
- processed file: `population.data`.
- details:
  - column `Provincias` corresponds to the province name;
  - column `Total` provides the total population.
- Official data from the [Instituto Nacional de Estadística](https://www.ine.es).

### Mobility data
- raw files (unzipped): `VI_J00.csv`, ..., `VI_J12.csv` and `VI_O00.csv`, ..., `VI_O15.csv`
- processed file: `province_mobility.data`
- details:
  - column `Origen` denotes the outbound province using the [INE's naming convention for the provinces]
  - column `Destino` denotes the inbound province using the [INE's naming convention for the provinces]
  - column `Viajeros` corresponds to the numbers of people that travel between these two autonomous communities.
- [original file](https://cdn.fomento.gob.es/portal-web-drupal/Docs_OTLE/matrices_julio_csv.zip) for July/August downloaded on 2020-08-11
- [original file](https://cdn.fomento.gob.es/portal-web-drupal/Docs_OTLE/matrices_octubre_csv.zip) for October downloaded on 2020-08-11

__Note__: The insular provinces are further subdivided into their islands:
  - 07 	Illes Balears: 07_1 Menorca, 07_2 Ibiza and 07_3 Mallorca
  - 35 Las Palmas: 35_1 Lanzarote, 35_2 Fuerteventura and 35_3 Gran Canaria
  - 38 Santa Cruz de Tenerife: 38_1 El Hierro, 38_2 Tenerife, 38_3 La Gomera and 38_4 La Palma

__Note__: more than one row may correspond to the same origin-destination pair since the original data breaks down the origin-destination journeys based on the period of the day as well as the means of transportation:
  - period of the day:
    - P1: 00:00 - 06:00
    - P2: 06:00 - 10:00
    - P3: 10:00 - 17:00
    - P4: 17:00 - 00:00
  - means of transportation:
    - roads: autobús, privado, carretera
    - seaways: barco
    - railways: tren
    - airways: avión

__Note__: numbers are represented using the Spanish convention where thousands are separated using a comma (ex: 100,000 denotes one hundred thousand)

## Publications

Please cite:

_Deep learning of contagion dynamics on complex networks_, arXiv:1904.10814.
<br>
[Charles Murphy*](https://scholar.google.ca/citations?user=xgBmSD8AAAAJ&hl=en&oi=sra),
[Edward Laurence*](https://edwardlaurence.me/),
[Antoine Allard*](http://antoineallard.info),
<br>
[arXiv](https://arxiv.org/abs/1904.10814)
