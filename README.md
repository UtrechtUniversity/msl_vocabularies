# MSL vocabularies

## About

This repository is used to store and provide access to the vocabularies used and maintained by the [EPOS Multi-Scale 
Laboratories (MSL) community](https://www.epos-eu.org/tcs/multi-scale-laboratories). The vocabularies are used at the 
[EPOS Multi-Scale Labs data catalogue](https://epos-msl.uu.nl/) to improve findability of data publications. We 
encourage others to use and improve the provided vocabularies within this repository.

## Vocabularies

We currently publish the following vocabularies:
- Analogue modelling of geological processes (referred to as "analogue")
- Field-Scale Laboratories
- Geochemistry
- ~~Geo-energy testbeds (referred to as "testbeds")~~ (Replaced by the Field-Scale Laboratories vocabulary starting version 1.4)
- Geological age
- Geological setting
- Materials
- Microscopy and tomography (referred to as "microscopy")
- Paleomagnetism
- Pore fluids
- Rock and melt physics (referred to as "rockphysics")

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
- external_uri; uri of term in external vocabulary
- external_vocab_scheme; scheme of external vocabulary

Sample of data:

        {
        "uri": "https:\/\/epos-msl.uu.nl\/voc\/materials\/1.4\/sedimentary_rock",
        "vocab_uri": "https:\/\/epos-msl.uu.nl\/voc\/materials\/1.4\/",
        "value": "sedimentary rock",
        "label": "sedimentary rock",
        "synonyms": [],
        "children": [
            {
                "uri": "https:\/\/epos-msl.uu.nl\/voc\/materials\/1.4\/sedimentary_rock-breccia",
                "vocab_uri": "https:\/\/epos-msl.uu.nl\/voc\/materials\/1.4\/",
                "value": "breccia",
                "label": "breccia",
                "synonyms": [],
                "children": [],
                "external_uri": "http:\/\/resource.geosciml.org\/classifier\/cgi\/lithology\/breccia",
                "external_vocab_scheme": "geosciml"
				...
            },
		"external_uri": "http:\/\/resource.geosciml.org\/classifier\/cgi\/lithology\/sedimentary_rock",
        "external_vocab_scheme": "geosciml"

### Excel

Excel exports are available in xlsx format.

### Turtle

Vocabularies are also published in turtle (Terse RDF Triple Language) format. Triples currently contain term uri, label and relational information.

Sample of data:

      <https://epos-msl.uu.nl/voc/materials/1.4/>
	  a skos:ConceptScheme ;
	  skos:prefLabel "Material" ;
	  skos:hasTopConcept <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock>, <https://epos-msl.uu.nl/voc/materials/1.4/igneous_rock_-_intrusive>, <https://epos-msl.uu.nl/voc/materials/1.4/igneous_rock_-_extrusive>, <https://epos-msl.uu.nl/voc/materials/1.4/metamorphic_rock>, <https://epos-msl.uu.nl/voc/materials/1.4/fault_rock>, <https://epos-msl.uu.nl/voc/materials/1.4/metasomatic_rock>, <https://epos-msl.uu.nl/voc/materials/1.4/meteorite>, <https://epos-msl.uu.nl/voc/materials/1.4/impact_rock>, <https://epos-msl.uu.nl/voc/materials/1.4/minerals>, <https://epos-msl.uu.nl/voc/materials/1.4/unconsolidated_sediment>, <https://epos-msl.uu.nl/voc/materials/1.4/analogue_modelling_material>, <https://epos-msl.uu.nl/voc/materials/1.4/synthesized_material> .

	<https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock>
	  a skos:Concept ;
	  skos:narrower <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-breccia>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-coal>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-conglomerate>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-dolomite>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-evaporite>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-marl>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-mudstone>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-sandstone> ;
	  skos:topConceptOf <https://epos-msl.uu.nl/voc/materials/1.4/> ;
	  skos:prefLabel "sedimentary rock" ;
	  rdfs:seeAlso <http://resource.geosciml.org/classifier/cgi/lithology/sedimentary_rock> ;
	  skos:exactMatch <http://resource.geosciml.org/classifier/cgi/lithology/sedimentary_rock> ;
	  dc:source "geosciml" ;
	  skos:inScheme <https://epos-msl.uu.nl/voc/materials/1.4/> .

	<https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone>
	  a skos:Concept ;
	  skos:narrower <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone-anstrude_limestone>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone-austin_limestone>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone-balmholtz_limestone>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone-carthage_limestone>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone-chalk>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone-chauvigny_limestone>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone-comiso_limestone>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone-estaillades_limestone>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone-fontvieille_limestone>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone-hallekis_limestone>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone-holston_limestone>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone-indiana_limestone>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone-irondequoit_limestone>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone-leitha_limestone>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone-lueders_limestone>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone-majella_limestone>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone-red_oland_limestone>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone-reynales_limestone>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone-saint_maximin_limestone>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone-shelly_limestone>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone-solnhofen_limestone>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone-tavel_limestone>, <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock-limestone-travertine> ;
	  skos:broader <https://epos-msl.uu.nl/voc/materials/1.4/sedimentary_rock> ;
	  skos:prefLabel "limestone" ;
	  rdfs:seeAlso <http://resource.geosciml.org/classifier/cgi/lithology/limestone> ;
	  skos:exactMatch <http://resource.geosciml.org/classifier/cgi/lithology/limestone> ;
	  dc:source "geosciml" ;
	  skos:inScheme <https://epos-msl.uu.nl/voc/materials/1.4/> .

### Rdf/xml

RDF/XML format published containing the same structural information as published within the turtle format.

## Contact

Questions, suggestions or contributions? Contact [Laurens Samshuijzen](mailto:l.samshuijzen@uu.nl).

