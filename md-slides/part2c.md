## Quality control tools and procedures

- _Perception: Anybody can edit anything - so Wikidata is no reliable source of knowledge_
- Seen as a threat for information systems based on Wikidata
  - particularly by some large Wikipedias (e.g., the English one)
- Basic policy to address this: Statements should be referenced

Note: Contradicting sources possible. Falsified statements can be deprecated.

---

## QA support for editors

- Contraint definition for properties
  - raise warnings during data input, when, e.g.
    - a format definition (ISBN, DOI etc.) is violated
    - a supposedly unique identifier is added to more than one item
  - generated lists of constraint violations (e.g. [ZDB ID format](https://www.wikidata.org/wiki/Wikidata:Database_reports/Constraint_violations/P1042#Format))
- Constraints can be very helpful, but do not cover complex cases

---

### More QA support for editors

- Additional reports can be created via SPARQL queries
- Shape Expressions (ShEx) allow to define complex constraints and conformance checks
  - [ShEx Primer](http://shex.io/shex-primer/)
  - [How to get started with Shape Expressions in Wikidata?](https://www.wikidata.org/wiki/Wikidata:WikiProject_ShEx/How_to_get_started%3F)

Note: ShEx can also be used to define views on to the data, which can exist in parallel to other views

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

[![revision history gandhi](images/revision_history_gandhi1.png)](https://www.wikidata.org/w/index.php?title=Q1001&action=history)

---

## Automated tools for vandalism detection

- Fighting to keep up with rate of human edits in Wikidata (multiple per second)
- ... requires reducing the manual workload, e.g. via
  - [Wikidata Abuse Filter](https://www.wikidata.org/wiki/Wikidata:Abuse_filter)
  - Objective Revision Evaluation Service ([ORES](https://www.wikidata.org/wiki/Wikidata:ORES))
- and other rule-based and machine-learning tools

---

### Ongoing research

- [Heindorf et al.: Vandalism Detection in Wikidata](https://groups.uni-paderborn.de/fg-engels/publications_pdfs/Konferenzbeitraege/heindorf2016_CIKM.pdf)
- [Sarabadani et al.: Building automated vandalism detection tools for Wikidata](https://arxiv.org/pdf/1703.03861)


