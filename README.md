# CFD Workspace Layout

This directory contains all CFD-related work. The structure is intentional.

## repos/  — source code (mostly read-only)
- Cloned git repositories (e.g., SU2, OpenFOAM utilities, mesh tools).
- Keep clean:
  - Do NOT run simulations here.
  - Do NOT commit unless developing solver source code.
- If something breaks, delete and reclone.

## runs/   — simulations and results
- All CFD cases live here.
- Contents typically include:
  - Configuration files (.cfg)
  - Mesh files (.su2, .msh, etc.)
  - Solver outputs, logs, history files, and visualization files
- Safe to modify, rerun, or delete.

## scripts/ — automation and post-processing
- Helper scripts for:
  - Parametric sweeps
  - Job submission
  - Post-processing and plotting
- Can be split by solver (su2/, openfoam/, shared/).

### Core rule
repos = code  
runs  = data  
scripts = logic

Do not mix these roles.
