
# Real-Time Soccer Match Data Streaming (Python, Spring 2025)

This project implements a real-time ingestion pipeline that retrieves live soccer match data from an external API, normalizes the responses, and streams structured records into Kafka. It demonstrates practical skills in API-driven data collection, real-time streaming, and building pipelines suitable for downstream analytics.

---

## Project Objectives

- Normalize varying API responses into a consistent, analysis-ready schema.
- Stream event-level data in real time rather than capturing periodic snapshots.
- Apply principles used in modern data engineering workflows, including modular extraction, transformation, and transport.
- Demonstrate the ability to refine parsing logic when external data sources change or return inconsistent fields.

---

## Technologies Used

- **Python**
- **Requests** for API ingestion
- **Kafka** for real-time streaming
- **JSON normalization** and schema design
- **NC State University HPC** as the execution environment

---

## Repository Structure

```
/
├── src/
│   ├── fetch_live_events.py     # API polling and ingestion
│   ├── normalize.py             # JSON cleaning and structuring
│   └── stream_to_kafka.py       # Kafka producer logic
├── config/
│   └── example_config.json      # Placeholder for user credentials/settings
└── README.md
```

---

## Running the Project

This project was originally executed on the NC State University High-Performance Computing (HPC) cluster. You may adapt it to any standard Linux environment with Python and Kafka installed.

### HPC Access (Example)

```bash
ssh -N -L 9999:login01:1113 <your_id>@login.hpc.ncsu.edu
```

Then access Jupyter (if applicable):

```
http://localhost:9999/tree?token=<your_token>
```

### Local Execution

1. Install Python dependencies listed in `requirements.txt` (if provided).
2. Start a local Kafka broker.
3. Create a config file containing your API credentials.
4. Run the ingestion components individually or via your orchestrator of choice.

**Important:**  
This repository does **not** contain any API keys, tokens, or Kafka credentials. You must supply your own in a local configuration file.

---

## Notes

- Code is organized to reflect production-oriented data pipeline patterns.
- The normalization logic is designed to be transparent and adaptable as API fields change.
- Kafka is used to simulate a scalable event-streaming workflow consistent with modern audit, analytics, and ingestion systems.
