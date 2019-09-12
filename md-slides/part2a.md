# Wikidata as linking hub

---

## The idea of linking hubs

Connect concepts via identifiers/URLs

![hub](https://i.imgur.com/dgRaN33.png)

Existing hubs: [VIAF](http://viaf.org), [sameAs.org](http://sameas.org), ...

<small>Image by Jakob Voss</small>

Note:
Main advantage of a linking hub is that it requires far less links between the individual data points.

Links in pre-existing hubs are collected or derived algorigoritmically. Wikidata in contrast works as a curated hub. Links can be added or amended by everybody who cares.

---

## Different linking properties

1. [equivalent class](https://www.wikidata.org/wiki/Property:P1709 (datatype URL))
3. [exact match](https://www.wikidata.org/wiki/Property:P2888) (datatype URL)
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

#### Example at item [Assessment center](https://www.wikidata.org/wiki/Q265558)

![assesment](images/mapping_relation_assessment_center.png)

---

## How does that relate to the Linked Data model?

Internal data model and storage (Wikibase) is transformed to RDF for:
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

Note: The identifier with the string value External-ID is published as this
URI, but not with a general-understood property such as schema:sameAs or
umbel:isLike.

---

## Federated SPARQL queries

Example: GND authority has information about the professions/occupations of people which are not known in wikidata.

So get that information dynamically from a GND SPARQL endpoint.

Here, we are interested in economists, in particular.

---

### From Wikidata to a remote endpoint

[query to WDQS](https://w.wiki/89A)

### From a remote endpoint to Wikidata

[query to GND endpoint](http://zbw.eu/beta/sparql-lab/?endpoint=http://zbw.eu/beta/sparql/gnd/query&queryRef=https://api.github.com/repos/zbw/sparql-queries/contents/gnd/wd_occupation_economist.rq)

---

### Several points for attention

- To reach out from Wikidata, endpoints have to be [approved](https://www.wikidata.org/wiki/Wikidata:SPARQL_federation_input) - [list](https://www.mediawiki.org/wiki/Wikidata_Query_Service/User_Manual/SPARQL_Federation_endpoints)
- In the other direction, access is normally not restricted
- Some federated queries get extremely slow, when large sets of bindings exist before the remote service is invoked
- be sure to exclude variables bound to blank nodes ('unknown value' in Wikidata)

---

## Further reading on Wikidata/RDF

- [RDF dump format (documentation)](https://www.mediawiki.org/wiki/Wikibase/Indexing/RDF_Dump_Format)
- [Waagmester: Integrating Wikidata and other linked data sources - Federated SPARQL queries](http://sulab.org/2017/07/integrating-wikidata-and-other-linked-data-sources-federated-sparql-queries/) ([more examples](https://www.wikidata.org/wiki/Wikidata:SPARQL_query_service/Federated_queries))
- [Malyshev et al.: Semantic Technology Usage in Wikipedia’s Knowledge Graph](https://iccl.inf.tu-dresden.de/w/images/5/5a/Malyshev-et-al-Wikidata-SPARQL-ISWC-2018.pdf)
- Critical comments/suggestions: [Freire/Isaac: Technical usability of Wikidatas linked data](https://pdfs.semanticscholar.org/f6d1/6eaf975af03a172c73843ff506592c952a04.pdf)

---

## Application process for a new property

...

[example](https://www.wikidata.org/wiki/Wikidata:Property_proposal/STW_Thesaurus_for_Economics_ID)


---

## Wikidata as a universal linking hub

- easy extensibility with new properties for external identifiers
- immense fund of existing items, with the full set of SKOS mapping relations for more or less exact mappings to these
- immediate extensibility with new items

Note: To sum up so far: Three characteristics make Wikidata suitable as an universal linking hub for the vast diversity of knowledge organization systems
