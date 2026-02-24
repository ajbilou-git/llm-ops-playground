# Sample Data

This directory stores generated sample data for the enterprise simulation.

## Data Generation

Each lab includes instructions to generate synthetic data. General approach:

```bash
cd labs/lab-XX-name/
python generate_data.py
```

## Data Categories

| Category | Format | Description |
|----------|--------|-------------|
| `tickets/` | JSON | Maintenance tickets (incidents, requests, history) |
| `docs/` | Markdown/PDF | Technical procedures, manuals, safety norms |
| `equipment_logs/` | CSV/Parquet | Sensor time series (vibration, temperature, pressure) |
| `knowledge_base/` | Markdown | FAQ, best practices, lessons learned |
| `assets/` | JSON | Equipment registry, parts, suppliers |

## Important

- Raw and processed data directories are gitignored
- Sample data generators are included in each lab
- Do not commit real enterprise data
