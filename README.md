# NewspaperMetadata

This repository contains automatically and manually generated metadata about historical newspapers.  Besides merging related fields from the source data	, the primary addition we made in this project was standardizing the identifiers for places of publication, following the Library of Congress in linking to records in (https://dbpedia.org/)[DBpedia].  We then joined these identifiers with DBpedia to include point longitude and latitude.

The basic metadata comes from the public catalogues of several newspaper digitization and aggregation projects:

* Chronicling America
* Trove
* Gale US and UK newspapers
* Europeana
* Delpher
* American Periodicals Series

Currently, the JSON and CSV files contain the following fields:

Field | Description
---- | -----
`series` | unique identifier for a newspaper series, usually derived from existing identifiers such as LCCN numbers
`title` | title of series
`lang` | common languages in the series, according to catalogue data; in JSON, an array; in CSV, a semicolon-delimited list
`publisher` | series publisher
`placeOfPublication` | listed place of publication
`coverage` | link to a https://dbpedia.org/ entry for the place of publication
`lon` | DBpedia decimal longitude
`lat` | DBpedia decimal latitude
`subcollection` | series type

