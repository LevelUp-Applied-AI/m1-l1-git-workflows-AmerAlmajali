# CHANGELOG

## [2026-03-11] — Collaboration setup and project integration

### Added
- Project scaffold: README.md, .gitignore, requirements.txt, setup.sh 
- AGENTS.md: AI contribution policy defining testing requirements, secrets policy, scope boundaries, and reproducibility standards
- setup.sh: idempotent environment setup script for automated project initialization
- CHANGELOG.md: project change history file
- - test_environment.py: environment validation script
### Changed
- README.md: rewritten and expanded with full project documentation including project overview, setup instructions, project structure, and contributing guidelines
- .gitignore: expanded to include patterns for secrets, data files, and OS artifacts  
  (.env, *.csv, *.parquet, *.xlsx, data/raw/, .DS_Store)
- Repository documentation improved to support new collaborators joining the project

### Notes
- Setup process can now be completed with a single command: ./setup.sh
- Repository prepared for collaborative development and AI-assisted contributions


## [2026-03-10] — Core Skills Drill: Git workflow and environment setup

### Added
- Python virtual environment `.venv` for isolated dependency management
- Branch setup/environment created for the assignment workflow


### Verified
- Python environment validated with:
  `python test_environment.py"`
- Git workflow tested: clone → branch → commit → push → pull request

### Notes
- Autograder checks confirmed:
  - Required files present : requirements.txt, README.md, .gitignore, test_environment.py all exist in the repo
  - requirements.txt contains required packages: pandas and matplotlib appear in the file (case-insensitive)
  - .gitignore excludes .venv/: 	.venv or .venv/ appears in .gitignore
  - test_environment.py passes : 	Script runs with exit code 0 and stdout contains Environment OK
  - README.md is non-empty:	File is more than 50 bytes (i.e., not just a blank title line)