# MA-Ontology

Planning Ontology extension for Multi-Agent Path Finding

Explainable MAPF Dashboard – [https://ai4society.github.io/ma-planning-ontology/](https://ai4society.github.io/ma-planning-ontology/)

---

## Running the Integration Script

The script `integrate_mapf.py` converts MAPF JSON logs into RDF/TTL instances aligned with the MA-Ontology.

### Usage

```bash
python integrate_mapf.py --log_file <json_log_file> [--ontology <ontology_file>] [--output <output_file>]
```

* `--log_file` (required): Path to the JSON log file (e.g., `log_files/robo_lab_2.json`)
* `--ontology` (optional): Path to the base ontology TTL file. Defaults to `./ontology/ma-ontology.ttl`.
* `--output` (optional): Path for the output TTL file. Defaults to `./generated_kg/mapf_instance.ttl`.

### Repository Structure

* **`log_files/`** → contains sample MAPF JSON log files
* **`generated_kg/`** → contains sample generated TTL knowledge graphs

### Examples

Run with sample logs and generate TTL files in the `generated_kg/` folder:

```bash
python integrate_mapf.py --log_file log_files/robo_lab_2.json --output generated_kg/robo_lab_2.ttl
# Knowledge graph successfully generated at 'generated_kg/robo_lab_2.ttl'

python integrate_mapf.py --log_file log_files/icbs_map_7_2.json --output generated_kg/icbs_7_2.ttl
# Knowledge graph successfully generated at 'generated_kg/icbs_7_2.ttl'

python integrate_mapf.py --log_file log_files/robo_lab_1.json --output generated_kg/robo_lab_1.ttl
# Knowledge graph successfully generated at 'generated_kg/robo_lab_1.ttl'
```

After running, you will find the generated `.ttl` knowledge graph files inside the `generated_kg/` folder.
