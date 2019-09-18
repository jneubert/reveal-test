## Wikidata as backbone for applications

---

### Digital preservation

File formats, software, emulator configurations, ...

Portal: [Wikidata for Digital Preservation](https://wikidp.org/)

[![wikidp](images/wikidp_org.png)](https://wikidp.org)

---

More info on Wikidata for digital preservation:
- [SWIB18 presentation](https://swib.org/swib18/slides/1_samuel_documenting-and-preserving.pdf)
- [SPARQL Query collection](https://www.wikidata.org/wiki/User:YULdigitalpreservation#Subpages)

---

## Item creation "on the go"

- With Mix-n-match "New item": rudimentary, no references
- Custom list of prepared QuickStatements insert blocks
- {Porto, slide 18}
- Workflow-wise, use same sequence for M-n-m input and prepared insert blocks

---

## Recommendations for item creation

- Pay attention to [Wikidata's notability criteria](https://www.wikidata.org/wiki/Wikidata:Notability)
- Explain your plan and ask for feedback in the [Wikidata project chat](https://www.wikidata.org/wiki/Wikidata:Project_chat)
- [Apply for a bot account](https://www.wikidata.org/wiki/Wikidata:Requests_for_permissions/Bot) to make mass edits ([example]())
- Source every statement ([hints]())
- Create input in [QuickStatements text format]()
- Run as batch, document input and batch URL

---

## Matching from WD to GND

- {SWIB17 breakout slides}

---

## Quality control tools and procedures

- Perception: Everybody can edit ererything - no reliable source
- Patroling
- Versioned edits and version control - technically very easy to revert edits ([example]())
- Vandalism prevention and monitoring of suspect edits (e.g., "new editor deleteing statements")

---

- Contraint definition for properties
  - raise warnings during data input, when e.g.
    - a format definition (ISBN, DOI etc.) is violated
    - a supposedly unique identifier is added to more than one item
  - generated lists of constraint violations (e.g. ???)
- Can be very helpful, but does not cover complex cases
- Additional reports can be created via SPARQL queries
- Shape Expressions (ShEx) allow to define complex constraints

---

## Community

---

## Wikiprojects

---
