# MSL vocabularies

## About

This repository is used to store and provide access to the vocabularies used and maintained by the [EPOS Multi-Scale 
Laboratories (MSL) community](https://www.epos-eu.org/tcs/multi-scale-laboratories). The vocabularies are used at the 
[EPOS Multi-Scale Labs data catalogue](https://epos-msl.uu.nl/) to improve findability of data publications. We 
encourage others to use and improve the provided vocabularies within this repository.

## Vocabularies

We currently publish the following vocabularies:
- analogue
- geochemistry
- geologicalage
- geologicalsetting
- materials
- microscopy
- paleomagnetism
- porefluids
- rockphysics

## Repository structure

Within the vocabularies folder all vocabularies are published in separate folders per vocabulary. Within the specific 
vocabulary folders a specific directory per version is published.

## Formats

We currently provide 4 formats for publishing the vocabularies:
- Json (.json)
- Excel (.xlsx)
- turtle file (.ttl)
- rdfxml (.xml)

### JSON

JSON (JavaScript Object Notation) format to provide easy access for (web)applications to use the data. The structure of the vocabularies are provided by including the child terms within its parent term. For each term the following are provided:
- uri; uri of term (Uniform Resource Identifier)
- vocab_uri; uri of vocabulary
- value; term
- label; label of term
- synonyms; array of synonyms
- children; child terms

Sample of data:

        "uri": "https:\/\/epos-msl.uu.nl\/voc\/analoguemodelling\/1.0\/modeled_structure",
        "vocab_uri": "https:\/\/epos-msl.uu.nl\/voc\/analoguemodelling\/1.0\/",
        "value": "Modeled structure",
        "label": "Modeled structure",
        "synonyms": [],
        "children": [
            {
                "uri": "https:\/\/epos-msl.uu.nl\/voc\/analoguemodelling\/1.0\/modeled_structure-modelled_magmatic_structure",
                "vocab_uri": "https:\/\/epos-msl.uu.nl\/voc\/analoguemodelling\/1.0\/",
                "value": "modelled magmatic structure",
                "label": "modelled magmatic structure",
                "synonyms": [],
                "children": [

### Excel

Excel exports are available in xlsx format.

### Turtle

Vocabularies are also published in turtle (Terse RDF Triple Language) format. Triples currently contain term uri, label and relational information.

Sample of data:

      <https://epos-msl.uu.nl/voc/analoguemodelling/1.0/modeled_structure-modelled_deformation_structure-modelled_crack>
        a skos:Concept ;
        skos:broader "https://epos-msl.uu.nl/voc/analoguemodelling/1.0/modeled_structure-modelled_deformation_structure" ;
        rdfs:label "modelled crack" .

      <https://epos-msl.uu.nl/voc/analoguemodelling/1.0/modeled_structure-modelled_deformation_structure-modelled_fracture>
        a skos:Concept ;
        skos:broader "https://epos-msl.uu.nl/voc/analoguemodelling/1.0/modeled_structure-modelled_deformation_structure" ;
        rdfs:label "modelled fracture" .

### Rdf/xml

RDF/XML format published containing the same structural information as published within the turtle format.

## Contact

Questions, suggestions or contributions? Contact [Laurens Samshuijzen](mailto:l.samshuijzen@uu.nl).

