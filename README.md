# MA-Ontology
Planning Ontology extension for Multi-Agent Path Finding

Explainable MAPF Dashboard – [https://ai4society.github.io/ma-planning-ontology/](https://ai4society.github.io/ma-planning-ontology/)

---

## Running the Integration Script

The script `integrate_mapf.py` converts MAPF JSON logs into RDF/TTL instances aligned with the MA-Ontology.

### Usage

```bash
python integrate_mapf.py <json_log_file> [--ontology <ontology_file>] [--output <output_file>]
