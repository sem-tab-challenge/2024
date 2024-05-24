# Metadata to KG Track Round 2 Datasets

In this round, a JSONL file is provided with each line representing a column in a table, along with table name, column name, and other columns in the same table. The goal is to map each such column to one "business glossary" item. We have also provided the metadata as well as the glossary in the form of an OWL ontology, to facilitate the mapping using ontology matching tools.

Sample data:
- [Sample Metadata File in JSONL](r2_sample_metadata.jsonl)
- [Sample Metadata Ontology in OWL](r2_sample_metadata.owl)
- [Sample Ground Truth](r2_sample_GT.csv)
- [Sample Output of Mapping](r2_sample_output.jsonl)
  - Note: The mappings array to be sorted in descending order by score.

Test data (what we expect you to map to the glossary):
- [Metadata File in JSONL](r2_test_metadata.jsonl)
- [Metadata Ontology in OWL](r2_test_metadata.owl)

Glossary:
- [Glossary in JSONL](r2_glossary.jsonl)
- [Glossary in OWL](r2_glossary.owl)
  - Note that unliked Round 1 data, this is a custom glossary and not derived from an existing publicly available KG.

Evaluation script:
- To try the evaluation script over the provided sample input/output, go to the data folder and run:
```
python evaluate.py -m r2_sample_output.jsonl -g r2_sample_metadata_GT.csv
```
