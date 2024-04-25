# Metadata to KG Track Datasets

## Round 1

In this round, a JSONL file is provided with each line representing a column in a table, along with table name, column name, and other columns in the same table. The goal is to map each such column to one DBpedia ontology property. We have also provided the metadata in the form of an OWL ontology, to facilitate the mapping using ontology matching tools.

Sample data:
- [Sample Metadata File in JSONL](r1_sample_metadata.jsonl)
- [Sample Metadata Ontology in OWL](r1_sample_metadata.owl)
- [Sample Ground Truth](r1_sample_GT.csv)
- [Sample Output of Mapping](r1_sample_output.jsonl)
  - Note: The mappings array will be sorted in descending order by score.

Test data (what we expect you to map to the glossary):
- [Metadata File in JSONL](r1_test_metadata.jsonl)
- [Metadata Ontology in OWL](r1_test_metadata.owl)

Glossary:
- [Glossary in JSONL](r1_glossary.jsonl)
- [Glossary in OWL](r1_glossary.owl)
  - Note that this is a representation of all the DBpedia properties as classes with one label and one description only. You can also use the full DBpedia OWL ontology that can be found [here](https://github.com/dbpedia/dbpedia/tree/master/ontology) but you need to ensure that you only map to properties.

Evaluation script:
- To try the evaluation script over the provided sample input/output, go to the data folder and run:
```
python evaluate.py -m r1_sample_output.jsonl -g r1_sample_metadata_GT.csv
```
