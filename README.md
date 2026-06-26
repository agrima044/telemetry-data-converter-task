# Telemetry Data Converter

Deloitte Technology Virtual Experience Programme — Software Engineering Task

## Overview

This project converts IoT device telemetry data from two different JSON formats into a single standardised output format.

## Project Structure

```
project/
│
├── index.html          ← Live results page (GitHub Pages)
├── style.css           ← Stylesheet
├── script.js           ← JavaScript
│
├── python-version/     ← Python source code
│   ├── main.py
│   ├── data-1.json
│   ├── data-2.json
│   └── data-result.json
│
└── README.md
```

## How It Works

**Format 1** stores location as a single slash-separated string and uses `operationStatus` and `temp` field names.

**Format 2** stores device info nested under a `device` object and uses an ISO 8601 timestamp string.

Both are converted to a standardised structure with a nested `location` object, Unix millisecond timestamp, and a `data` object with `status` and `temperature`.

## Running Python Tests

```bash
cd python-version
python3 main.py
```

All 3 tests pass:
- `test_sanity` — validates the expected result structure
- `test_dataType1` — converts Format 1 successfully
- `test_dataType2` — converts Format 2 successfully

## Live Demo

https://left-concerned-gnudebugger--kuhu04.replit.app
