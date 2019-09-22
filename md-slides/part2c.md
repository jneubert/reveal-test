## Quality control tools and procedures

- Perception: Everybody can edit ererything - no reliable source
- Versioned edits and version control - technically very easy to revert edits ([example]())
- [Patroling](https://www.wikidata.org/wiki/Wikidata:Patrol)
- Vandalism prevention and monitoring of suspect edits (e.g., "new editor deleteing statements")

---

- Contraint definition for properties
  - raise warnings during data input, when, e.g.
    - a format definition (ISBN, DOI etc.) is violated
    - a supposedly unique identifier is added to more than one item
  - generated lists of constraint violations (e.g. ???)
- Can be very helpful, but does not cover complex cases
- Shape Expressions (ShEx) allow to define complex constraints
- Additional reports can be created via SPARQL queries


---

- [Heindorf et al.: Vandalism Detection in Wikidata](https://groups.uni-paderborn.de/fg-engels/publications_pdfs/Konferenzbeitraege/heindorf2016_CIKM.pdf)
- [Sarabadani et al.: Building automated vandalism detection tools for Wikidata](https://arxiv.org/pdf/1703.03861)
