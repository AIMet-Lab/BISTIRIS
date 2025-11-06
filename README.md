# BISTÌRIS Ontology & Knowledge Graph
<img src="https://raw.githubusercontent.com/AIMet-Lab/BISTIRIS/main/home/imgs/logo_bistiris.png" width="100" alt="Logo BISTIRIS">

<p align="justify"><strong>BISTÌRIS</strong> is a domain ontology and a curated knowledge graph designed to describe, compare, and analyse <strong>Sardinian traditional costumes</strong> and their parts, materials, colours, and provenance. The project supports cultural heritage documentation, enables semantic search and reasoning on costume‑features across regions and eras, and opens new avenues for education, tourism and heritage valorisation.</p>

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.15310350.svg)](https://doi.org/10.5281/zenodo.15310350)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

## Resources
- 🌐 [BISTÌRIS landing page](https://aimet-lab.github.io/BISTIRIS/home/index.html)
- 🌐 [Ontology Documentation](https://aimet-lab.github.io/BISTIRIS/docs/index-en.html)
- 📄 [Ontology file in OWL format](https://aimet-lab.github.io/BISTIRIS/bistiris_model.owl)
- 📄 [Data in RDF format](https://aimet-lab.github.io/BISTIRIS/bistiris_data.rdf)
- 📄 [VOID metadata file](https://aimet-lab.github.io/BISTIRIS/well-known/void.ttl)

## Base IRI
🔗 https://aimet-lab.github.io/BISTIRIS#

**Version:** 3.0

## Competency Questions Addressed
- How do costume and garment characteristics vary across different geographical areas of Sardinia?
- How do costume and garment characteristics vary over time?
- Do the costumes and garments share similar characteristics in nearby places?
- Which specimens of a given garment are constructed using transparent materials?
- Which garments are typically worn over others? For example, in which costumes is the bodice worn over the jacket?
- What is the frequency with which two specific properties occur simultaneously among the garments?

## Example of SPARQL queries addressed
- Which garments are typically worn over others? For example, in which costumes is the bodice worn over the jacket?
```
PREFIX bst: <https://aimet-lab.github.io/BISTIRIS#>
PREFIX dbo: <http://dbpedia.org/ontology/>
PREFIX schema: <https://schema.org/>
SELECT ?garment ?place
WHERE {
    ?garment a bst:F-Bodice ;
        bst:covers ?otherGarment .  
    ?otherGarment a bst:F-Jacket ;
      schema:fromLocation ?place .
      ?place a dbo:Place .
  }
```
For additional query examples, see [here](https://github.com/AIMet-Lab/BISTIRIS/tree/main/query).

## Authors
- Giorgio Corona  
- Dario Guidotti  
- Laura Pandolfo  
- Luca Pulina
  
## Contact
For more information:
- [lpandolfo@uniss.it](mailto:lpandolfo@uniss.it)
- [gcorona1@uniss.it](mailto:gcorona1@uniss.it)

© 2025 AIMET Lab – University of Sassari
