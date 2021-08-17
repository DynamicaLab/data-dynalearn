### Datasets used in the article "Deep learning of contagion dynamics on complex networks"

This repository contains the raw and processed datasets as well as the [notebook](covid-data-processing.ipynb) used to generate the latter.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.5015063.svg)](https://doi.org/10.5281/zenodo.5015063)

#### Number of cases
- raw file: `cases-timeseries-20210327.csv`
- processed file: `cases-timeseries.data`
- details:
  - column `provincia_iso` corresponds to the province using the [ISO 3166-2:ES] naming convention;
  - column `fecha` indicates the date in format `YYYY-MM-DD`;
  - column `num_casos` provides the number of daily new cases.
- official data from the [Centro Nacional de Epidemiología](https://cnecovid.isciii.es).
- [original file](https://cnecovid.isciii.es/covid19/resources/casos_tecnica_provincia.csv) downloaded on 2021-03-27.


#### Province population sizes
- raw file: `population-data.csv`.
- processed file: `population.data`.
- details:
  - column `Provincias` corresponds to the province name;
  - column `Total` provides the total population.
- official data from the [Instituto Nacional de Estadística](https://www.ine.es).
- [original file](https://www.ine.es/jaxiT3/Datos.htm?t=2917) for the year 2019 downloaded on 2020-08-11.


#### Mobility data
- raw files (unzipped): `VI_J00.csv`, ..., `VI_J12.csv` and `VI_O00.csv`, ..., `VI_O15.csv`
- processed file: `province_mobility.data`
- details:
  - column `Origen` denotes the outbound province using the [INE's naming convention for the provinces]
  - column `Destino` denotes the inbound province using the [INE's naming convention for the provinces]
  - column `Viajeros` corresponds to the numbers of people that travel between these two autonomous communities.
- official data from a pilot study done by the [Ministerio de Fomento](https://observatoriotransporte.mitma.gob.es/estudio-experimental).
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


#### Reference
_Deep learning of contagion dynamics on complex networks_<br>
[Charles Murphy](https://scholar.google.ca/citations?user=xgBmSD8AAAAJ&hl=en&oi=sra),
[Edward Laurence](https://edwardlaurence.me/) and
[Antoine Allard](http://antoineallard.info),<br>
[Nature Communications 12, 4720 (2021)](https://doi.org/10.1038/s41467-021-24732-2)


[ISO 3166-2:ES]: https://es.wikipedia.org/wiki/ISO_3166-2:ES
[INE's naming convention for the autonomous communities]: https://www.ine.es/daco/daco42/codmun/cod_ccaa.htm
[INE's naming convention for the provinces]: https://www.ine.es/daco/daco42/codmun/cod_provincia.htm
