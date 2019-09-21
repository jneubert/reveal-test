## Linking content via Mix-n-Match

---

Mix-n-match is a widely used tool (by Magnus Manske) to link external databases, catalogs, etc. to existing Wikidata items or to create new ones.

![map to hub](images/map_to_hub.png)

---

### Example list:

### Newspapers and journals<br />from the 20th Century Press Archive

Note: A few remarks on the domain: The archive contains thematically collected cclippings about persons, events, companies from the first half of the 20th century.

---

![gandhi nairobi](images/gandhi_nairobi.png)

Note: A glimpse into the folder about Mahatma Gandhi, the Indian indepence leader.

---

![gandhi shanghai](images/gandhi_shanghai.png)

Note: More than 1500 sources from many countries has been clipped for the thematic folders. Most of them are linked to the ZDB authority file, and by this identifier we can link them to Wikidata.

---

Please navigate to our [example catalog](https://tools.wmflabs.org/mix-n-match/#/catalog/2773)

[Mix-n-match manual](https://meta.wikimedia.org/wiki/Mix%27n%27match/Manual)

---

## Tasks

- Login through _Widar_
- In "Automatically matched" list:
  - Connect matching items
  - Remove non-matching entries
- In "Unmatched" list:
  - Search for existing items
  - Create missing items ([suggested properties](https://www.wikidata.org/wiki/Wikidata:WikiProject_Periodicals#Periodical_properties))

---

## Item creation "on the go"

- With Mix-n-match "New item": rudimentary, no references
- Custom list of prepared QuickStatements insert blocks
- {Porto, slide 18}
- Workflow-wise, use same sequence for M-n-m input and prepared insert blocks

---

## Recommendations for item creation

- Pay attention to [Wikidata's notability criteria](https://www.wikidata.org/wiki/Wikidata:Notability) (much more relaxed then Wikipedias)
- Explain your plan and ask for feedback in the [Wikidata project chat](https://www.wikidata.org/wiki/Wikidata:Project_chat)
- [Apply for a bot account](https://www.wikidata.org/wiki/Wikidata:Requests_for_permissions/Bot) to make mass edits ([example]())
- Source every statement ([hints]())
- Create input in [QuickStatements text format]()
- Run as batch, document input and batch URL

---

## Matching from WD to GND

- {SWIB17 breakout slides}

---

## Import catalog data to Mix-n-Match

---

### Prepare data 

... as tab-separated table (one line per record) with columns

1. identitfier
2. name
3. description

[Input file for the example used earlier](https://pm20.zbw.eu/work/mnm/publikation_zdb_mnm_edited.txt)

---

### Pay attention to

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


