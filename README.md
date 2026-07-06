## Global Roller Coasters Data Analyzer

Hi there! Welcome to this repository. 

I built this terminal-based data analyzer from scratch using **Python** to process and explore a global dataset of roller coasters. Instead of relying on heavy, pre-built libraries like Pandas, the challenge I gave myself here was building the entire data processing pipeline from the ground up by writing custom parsing engines to ingest raw CSV data, handling type casting, and implementing basic SQL-like filtering operations completely in Python.

The project is strictly modular, splitting responsibilities cleanly across three separate files to make the application reliable, easy to read, and maintainable.

### Tech & Design

* **Modular Python Architecture:** Engineered using a strict separation of concerns across a 3-tier architecture: `main_ajanel_giselle.py` (runtime workflow), `helper.py` (data ingestion and computational logic), and `user_io.py` (terminal display and user interface layer).
* **Custom CSV Data Pipeline:** Programmed a memory-efficient file-stream parsing algorithm that maps unstructured string arrays into dynamic list-of-dictionary structures using native string operations (`.strip()`, `.split()`).
* **Robust Type Checking & Aggregation:** Developed comparative filtering workflows that handle messy text data natively, leveraging methods like `.isdigit()` to isolate extreme values safely (like finding the loopiest or tallest coaster) without triggering runtime errors on missing fields.
* **File I/O Engine:** Integrated native file writing features to generate sorted, filtered reports (like isolating 700+ unique locations into a standalone `amusement_parks.txt` output file).

### File Structure
```
amusement-parks-analyzer/
├── main_ajanel_giselle.py   # Core runtime loop and menu navigation framework
├── helper.py                # Data ingestion engine and backend search logic
├── user_io.py               # Input/Output layer handling terminal menus and report saving
└── roller_coasters.csv      # Global unstructured dataset processed by the pipeline
```
