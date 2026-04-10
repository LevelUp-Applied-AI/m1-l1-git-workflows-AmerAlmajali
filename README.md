
# Module 1 — Integration Task: Integration-1-Dev-Environment

## Team Members
- Amer Almajali  
- Lina Haddad  
- Omar Qasem  


## Project Overview

This project sets up a collaborative Python development environment for new team members to quickly get started. The environment ensures that anyone can clone the repository, install dependencies, validate the setup, and begin contributing without manual configuration issues. The output is a fully functional project scaffold with a working virtual environment, structured directories, and automated setup scripts.

---


## Setup Instructions

Follow these commands to set up the project environment:
git clone https://github.com/LevelUp-Applied-AI/m1-l1-git-workflows-AmerAlmajali.git
cd m1-l1-git-workflows-AmerAlmajali
python -m venv .venv
Activate the environment depending on your platform.
Mac / Linux: ource .venv/bin/activate
Windows Git Bash: source .venv/Scripts/activate
Windows CMD: .venv\Scripts\activate.bat
Windows PowerShell: .venv\Scripts\Activate.ps1
Install dependencies:
pip install -r requirements.txt
Verify the environment:
python test_environment.py
Expected output:
Environment OK
You can also run the automated setup script:

chmod +x setup.sh
./setup.sh

---


## Project Structure


m1-l1-git-workflows-AmerAlmajali/
├── .git/                   — Git repository metadata
├── .github/                — GitHub configuration files
├── .venv/                  — Python virtual environment (ignored by Git)
├── tests/                  — Automated tests
├── .gitignore              — Files excluded from version control
├── AGENTS.md               — AI contribution policy
├── CHANGELOG.md            — Record of project changes
├── README.md               — Project documentation and setup guide
├── requirements.txt        — Python dependencies
├── setup.sh                — Automated environment setup script
└── test_environment.py     — Environment validation script


---

## Contributing

Branch naming conventions:


feature/<description>
fix/<description>
setup/<description>


Examples:


feature/data-cleaning
fix/setup-script
setup/environment-config


Contribution workflow:

1. Create a new branch
2. Implement the change
3. Run the environment verification
4. Commit with a clear message
5. Open a Pull Request

Example commit messages:


Add environment setup script
Fix environment validation issue
Update README setup instructions


On Windows systems, setup.sh should be executed using *Git Bash*, since it does not run directly in CMD or PowerShell.

