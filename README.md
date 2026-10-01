# Ontology-package

Tudalia Care Ontology — machine-readable care vocabulary for the AI engine:

**voice → STT → LLM → `validate_extraction()` → caregiver confirm → Senior Journal**

The engine only **proposes**. It never writes the care record by itself.

| | |
|---|---|
| Python package | [`packages/ontology-py`](packages/ontology-py) |
| Package docs | [`packages/ontology-py/README.md`](packages/ontology-py/README.md) |
| Version | **0.2.0** · vocabulary **2026.09.30-v0.2** |

---

## Layout

```
Ontology-package/
├── packages/ontology-py/   # installable Python package (vocabulary + validation)
├── reference/              # local docs / CSV (gitignored; optional)
└── README.md               # this file
```

---

## Quick start

```bash
cd packages/ontology-py
python3 -m venv .venv
source .venv/bin/activate
pip install -e ".[dev]"
pytest
```

### Run demos

```bash
cd packages/ontology-py
source .venv/bin/activate

# Valid / invalid concept objects (prints INPUT + OUTPUT)
python examples/validate_objects.py

# CLI sample extraction
python -m tudalia_ontology.demo

# Browser validation playground
python -m tudalia_ontology.validate_playground   # → http://127.0.0.1:8765
```

Full documentation, valid/invalid examples, and API usage: **[packages/ontology-py/README.md](packages/ontology-py/README.md)**.
