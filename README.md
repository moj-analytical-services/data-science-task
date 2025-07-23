# data-science-task

&nbsp;
#==============================================================================
# @author: Dr. Leila Yousefi 
#==============================================================================
&nbsp;



# Contents

* What the  for the Model does
* Why the for the Model is useful
* How users can get started with the  for the Model
* Where users can get help with  for the Model
* Who maintains and contributes to the  for the Model


&nbsp;
# [Repository and Git Setup](#setup) 

&nbsp;
# [Methods and Model](#summ) - summary of the quantitative methods used for modelling.  
&nbsp;   
# [Inputs](#inputs)
&nbsp;
# [Outputs](#outputs)
&nbsp;
# [Higher-level Process flow Diagrams](#high-process-flow) - proccess flow diagrames of main inputs/outputs for the Model.
&nbsp;
# [Aim](#aim) 
&nbsp;
# [Objectives](#objectives)
&nbsp;   
# [Background Knowledge](#Background)
&nbsp;
# [Control Assumptions and Sensitivity Analysis](#control-assumptions)
&nbsp;
# [Data Sources](#data-sources)
&nbsp;
# [Model Calculation](#calc-model) - details of model calculation
&nbsp;
# [Feature Engineering and Data Preparation](#preprocessing)
&nbsp;
# [Implementing the Demand Forecasting for LPA Model](#model) - details of model scripts
&nbsp;

&nbsp;
<a name="setup"></a>
# Repository and Git Setup

## Repository layout
project-name/
├── data/                    # raw & processed data (git-ignored)
│   ├── raw/                 # original, untouched data
│   └── processed/           # cleaned or transformed data outputs
├── notebooks/               # exploratory and analysis notebooks
│   └── data-analysis.ipynb  # data analysis notebook
├── src/                     # Python modules and scripts
│   ├── __init__.py          # marks this folder as a package
│   └── data_processing.py   # reusable data-loading and cleaning functions
│   └── data_quality.py      # Data Quality Checks class
├── tests/                   # Automated unit testing
│   └── test_data_quality.py # pytest tests for Data Quality
├─ .github/
│   └─ workflows/
│       └─ ci.yml 
├── .gitignore               # Configure to exclude from Git /data/, environment folders, caches, and any large files.
├── README.md                # project overview and setup instructions
└── requirements.txt         # pinned Python dependencies / freezed library versions to ensure consistent environments across machines.


## implementation
```bash
git clone git@github.com:your-org/project-name.git
cd project-name
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt


```
## Run tests locally
```bash
# Discover & run all tests in tests/
pytest --maxfail=1 --disable-warnings -q

```
or from Jupyter lab notebook: 
```python
!pytest -q
```

# Automate via CI (GitHub Actions)
Create a file .github/workflows/ci.yml:

# Discover & run all tests in tests/
pytest --maxfail=1 --disable-warnings -q
-q gives you a concise report.

On success you’ll see something like === 10 passed in 0.5s ===.

On failure you’ll get full assertion tracebacks
## Workflow

- data: place raw files in data/raw/.
- data: place cleaned / transformed data files in data/processed/.

- notebooks: work in notebooks/data_analysis.ipynb.

- modularise: once stable, move functions into src/.

- version: commit early & often:

- review: open a PR against main when ready.

```bash
git add .
git commit -m "EDA: initial missing-value summary"
git push origin main
```

- Version Control Workflow
    - Branching: Create a feature branch, e.g. feature/LY-analysis-01.
    - Commits: After each major step—EDA, modeling, evaluation—commit with a clear message:
    ```bash
    git add notebooks/01_analysis_template.ipynb src/data_processing.py
    git commit -m "EDA: added missing-value visualization"
    ```
    - Pull Request: When complete, open a PR against main and tag reviewers.

    - commit code + tests + requirements.
    
    - **CI**: add GitHub Actions workflow to enforce tests on every push.
    - Verify on GitHub: Navigate to the Actions tab of your repository on GitHub. You should see the “CI” workflow queued or running.
- Sharing with the Panel
    - Push your branch to GitHub: git push origin feature/analysis-X.
    - At discussion time, share the GitHub link to your notebook so the panel can view the commit history, code annotations, and outputs live.
    
- create the file if it doesn't exist
```bash
touch .gitignore
# Remove data/ from the index (but leave the files on disk)
git rm -r --cached data/
# Commit the change
git commit -m "Remove data folder from tracking per .gitignore"

python src/analyzers.py
```

&nbsp; 

<a name="summ"></a>
# Methods and Model 

&nbsp; 


**Aim:**

**Objective:**
1. 

2. 

3. 