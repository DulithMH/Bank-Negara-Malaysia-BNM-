# Data — Overview

Short description of the data: what it represents, units, collection method, temporal/spatial coverage, known caveats.

Files
- data/raw/ — raw, immutable files (large files should be handled with DVC or hosted externally)
- data/processed/ — cleaned, processed files used by notebooks/analysis

Provenance
- Source: where the raw data came from (links, access instructions)
- Steps: short summary of processing steps and the script/notebook that performs them (preferably code in src/)

Access/size
- If files are large, describe how to download them (script or external URL)
