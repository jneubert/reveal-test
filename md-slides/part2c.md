## Quality control tools and procedures

- _Perception: Anybody can edit anything - so Wikidata is no reliable source of knowledge_
- Seen as a threat for information systems based on Wikidata
  - particularly by some large Wikipedias (e.g., the English one)
- Basic policy to address this: Statements should be referenced

---

## QA support for editors

- Contraint definition for properties
  - raise warnings during data input, when, e.g.
    - a format definition (ISBN, DOI etc.) is violated
    - a supposedly unique identifier is added to more than one item
  - generated lists of constraint violations (e.g. ???)
- Constraints can be very helpful, but does not cover complex cases
- Shape Expressions (ShEx) allow to define complex constraints
- Additional reports can be created via SPARQL queries

---

## Revision control and patroling

- Versioned edits and version control
- Manual and tool supported vandalism prevention
- Watchlists
- Automated flagging of suspect edits (e.g., "new editor deleteing statements")
- [Patroling](https://www.wikidata.org/wiki/Wikidata:Patrol)
- Technically very easy to revert edits
- Semi-protection or protection of oftenly-vandalized items

Note: I'll give you an example of this - all on one page

---

![revision history gandhi](images/revision_history_gandhi1.png)

---

## Automated tools for vandalism detection

- Fighting to keep up with rate of human edits (multiple per second)
- Wikidata Abuse Filter
- Objective Revision Evaluation Service (ORES)

---

### Ongoing research

- [Heindorf et al.: Vandalism Detection in Wikidata](https://groups.uni-paderborn.de/fg-engels/publications_pdfs/Konferenzbeitraege/heindorf2016_CIKM.pdf)
- [Sarabadani et al.: Building automated vandalism detection tools for Wikidata](https://arxiv.org/pdf/1703.03861)


