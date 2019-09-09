# Wikidata as linking hub

---

## Linking hubs

Connect concepts via identifiers/URLs

![hub](https://i.imgur.com/dgRaN33.png)

Existing hubs: [VIAF](http://viaf.org), [sameAs.org](http://sameas.org), ...

<small>Image by Jakob Voss</small>

Note:
Main advantage of a linking hub is that it requires far less links between the individual data points.

Links in pre-existing hubs are collected or derived algorigoritmically. Wikidata in contrast works as a curated hub. Links can be added or amended by everybody who cares.

---

## Different linking properties

1. [equivalent class](https://www.wikidata.org/wiki/Property:P1709)
2. [equivalent property](https://www.wikidata.org/wiki/Property:P1628)
3. [exact match](https://www.wikidata.org/wiki/Property:P2888) (datatype URL)<br />
  generic link to URL in the meaning of _skos:exactMatch_
4. [Pxxxx](https://w.wiki/7qc): more than 4000 specialized properties (datatype external identifier)

---

## Examples for external identifiers

- GND / VIAF identifiers
- geogaphical entities
- proteins
- Swedish cultural heritage objects
- African plants
- baseball players
- TED conference speakers

---

![Agarwal page](https://i.imgur.com/VNaeUMK.jpg)

---

## Property definitions

- subject item for the property
- examples
- constraints on values, cardinality, etc.
- [formatter URL](https://www.wikidata.org/wiki/Property:P1630): creates a clickable link for the ID
- start at the property page https://www.wikidata.org/wiki/Property:{Pid}

---

## Property Documentation

[![ISSN property page](images/property_page.png)](https://www.wikidata.org/wiki/Property:P236)

---

[![ISSN property page](images/property_talk.png)](https://www.wikidata.org/wiki/Property_talk:P236)

Note:
- lots of interesting statistics
- number of current uses
- constraints (violation lists)
  - e.g., format, type

---

## Beyond sameness - mapping relations

- Wikidata external ids imply "sameness" of linked concepts
- even with geographic names, other mapping relations are required in some cases. 
- examples:
  - close matches, e.g., "Yugoslavia" (1918-1992) (Wikidata) ≅ "Yugoslavia (until 1990)" (STW)
  - related matches, e.g. a company and its founder

---

## Mapping relation type (P4390)

- introduced after a community discussion in October 2017
- to be used as _qualifier_ for external id entries
- fixed value set - SKOS mapping relations (exact, close, broad, narrow, related match)

---

#### Example at "Assessment center (Q265558)"

![assesment](images/mapping_relation_assessment_center.png)

---

## How does that relate to the Linked Data model?

Internal data model and storage (Wikibase) transformed to RDF
- [RDF dumps](https://www.wikidata.org/wiki/Wikidata:Database_download#RDF_dumps)
- [Query Service](https://query.wikidata.org)

---

## RDF linking from Wikidata

- [formatter URI for RDF resource](https://www.wikidata.org/wiki/Property:P1921): linked data URI<br />
e.g., http://sws.geonames.org/$1/, (vs. formatter URL https://www.geonames.org/$1)
- [List of 130+ relationships to external RDF datasets](https://w.wiki/7ts)
- [26+ million](https://lod-cloud.net/dataset/wikidata) linked external RDF resources
- plus ~950.000 [exact match]() relations to individual URIs

---

## Links in the RDF dumps

Output has full URLs to external resources, _however_ with Wikidata-specific
properties:

```
  wd:Q123 wdt:P234 "External-ID" ;
          wdtn:P234 <http://example.com/reference/External-ID>
```
This creates a hurdle for generic Linked Data browsers and tools - not even 
[exact match](https://www.wikidata.org/wiki/Property:P2888) is translated to
skos:exactMatch

---

## Federated SPARQL queries

...

---

## Further reading on Wikidata/RDF

- [RDF dump format (documentation)](https://www.mediawiki.org/wiki/Wikibase/Indexing/RDF_Dump_Format)
- [SPARQL federation](https://www.wikidata.org/wiki/Wikidata:SPARQL_federation_input) ([examples](https://www.wikidata.org/wiki/Wikidata:SPARQL_query_service/Federated_queries))
- [Malyshev et al.: Semantic Technology Usage in Wikipedia’s Knowledge Graph](https://iccl.inf.tu-dresden.de/w/images/5/5a/Malyshev-et-al-Wikidata-SPARQL-ISWC-2018.pdf)
- Critical comments/suggestions: [Freire/Isaac: Technical usability of Wikidatas linked data](https://pdfs.semanticscholar.org/f6d1/6eaf975af03a172c73843ff506592c952a04.pdf)

---

## Application process for a new property

...

[example](https://www.wikidata.org/wiki/Wikidata:Property_proposal/STW_Thesaurus_for_Economics_ID)


---

## Linking content via Mix-n-Match

---

Please navigate to our [example catalog](https://tools.wmflabs.org/mix-n-match/#/catalog/2773)

[Mix-n-match manual](https://meta.wikimedia.org/wiki/Mix%27n%27match/Manual)

---

## Import catalog data to Mix-n-Match

---

### Prepare data 

... as tab-separated table (one line per record) with columns

1. identitfier
2. name
3. description

[example file](https://pm20.zbw.eu/work/mnm/publikation_zdb_mnm_edited.txt)

Pay attention to

- description column: include everything useful for intelectual identification
- order: may structure your workflow (e.g., most used entries first)

---

### Load data via web interface

... at https://tools.wmflabs.org/mix-n-match/import.php

---

![mnm import](images/mnm_import.png)

---

![mnm import](images/mnm_import_2_crop.png)

---

![mnm import](images/mnm_import_result.png)

---

![mnm import](images/mnm_catalog_initial.png)

---

### Sync existing ids from Wikidata

![mnm sync](images/mnm_sync_catalog.png)

---

![mnm sync](images/mnm_sync.png)

---

![mnm after sync](images/mnm_catalog_after_sync.png)

---

# Misc

---

## Wikidata as backbone for applications

---

### Scholia

---

### Digital preservation

File formats, software, emulator configurations, ...

Portal: [Wikidata for Digital Preservation](https://wikidp.org/)

More info:
- [SWIB18 presentation](https://swib.org/swib18/slides/1_samuel_documenting-and-preserving.pdf)
- [SPARQL Query collection](https://www.wikidata.org/wiki/User:YULdigitalpreservation#Subpages)

---


