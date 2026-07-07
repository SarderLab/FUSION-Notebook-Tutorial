# FUSION++ Notebook Tutorial

This repository contains a beginner-friendly Jupyter notebook for running the FUSION++ pipeline.

FUSION++ helps users work with HuBMAP and FUSION data inside a notebook environment. The notebook guides users through data access, analysis jobs, visualization, and downstream exploration.

## Where can users access the data?

Users can access data from two main places:

1. **[HuBMAP Data Portal](https://portal.hubmapconsortium.org/)**

   Use this to search for public HuBMAP datasets and copy the HuBMAP dataset ID.

2. **[FUSION Platform](https://fusionpub.rc.ufl.edu)**

   Use this to view, manage, visualize, and process image and analyze data connected to the FUSION workflow.

## Accessing Data from FUSION

To access data from FUSION:

1. Go to [fusionpub.rc.ufl.edu](https://fusionpub.rc.ufl.edu).
2. Navigate to one of the following folders:

```text
FUSION_Kidney_Visium → Visium → Visium Frozen
```

or

```text
FUSION_Kidney_Visium → Visium → Visium FFPE
```

These folders contain the FUSION datasets that can be used with the notebook.
 > For a more detailed explanation, refer to the sub-section 1.2 in Data Management Features in the Notebook.

## Accessing Data from HuBMAP

To access data from HuBMAP:

1. Go to [portal.hubmapconsortium.org](https://portal.hubmapconsortium.org/).
2. Select **Datasets** from the navigation menu.
3. Browse or search for the dataset or datasets you want to use and copy the HuBMAP_ID.
 > For a more detailed explanation, refer to the sub-section 1.1 in Data Management Features in the Notebook.

## Running the Notebook on HiPerGator

Use this option if you are working on the University of Florida HiPerGator environment.

### Step 1: Open a terminal on HiPerGator

Open a terminal in your HiPerGator Jupyter session or through the HiPerGator command line.

### Step 2: Create a virtual environment

```bash
python -m venv fusion_env
```

This creates a new Python environment named `fusion_env`.

### Step 3: Activate the virtual environment

```bash
source fusion_env/bin/activate
```

After activation, your terminal should show something like:

```bash
(fusion_env)
```

This means the environment is active.

### Step 4: Install the FUSION++ package from GitHub

```bash
pip install "git+https://github.com/SarderLab/fusion-packages.git"
```

This installs the required FUSION++ package directly from GitHub.

### Step 5: Install ipykernel

```bash
pip install ipykernel
```

`ipykernel` allows this virtual environment to appear as a selectable kernel inside Jupyter.

### Step 6: Create a Jupyter kernel

```bash
python -m ipykernel install --user --name fusion_env --display-name "FUSION"
```

This creates a new notebook kernel named:

```text
FUSION
```

### Step 7: Open the notebook

Open:

```text
fusion_demo.ipynb
```

Then select the kernel:

```text
FUSION
```

### Step 8: Run the notebook

Run the notebook cells from top to bottom.

The notebook will guide you through:

1. Initial setup and authentication
2. Selecting a HuBMAP dataset
3. Downloading or accessing data
4. Running analysis jobs
5. Viewing outputs
6. Visualizing results

## Running the Notebook on HuBMAP Workspace

Use this option if you are working inside a HuBMAP Workspace.

HuBMAP Workspaces provide a browser-based JupyterLab environment where users can explore HuBMAP data and run notebooks.

To use the notebook inside a HuBMAP Workspace:

1. Open the HuBMAP Consortium Website - [portal.hubmapconsortium.org](https://portal.hubmapconsortium.org/).
2. Open the **Data Portal** and login to your account.
3. Open **My Workspaces** and select the `Create New` button.
4. Scroll through the Templates and select **FUSION++**.
5. This will take you to the fusion_demo notebook, which will guide you through the workflow.

## Basic Workflow

The general workflow of the notebook is:

```text
Initial Setup & Authentication
        ↓
Data Management
(Download / Upload / Prepare Data)
        ↓
Run Analysis Jobs
        ↓
Visualization
```

## Expected Output Folder Structure

After running the notebook, outputs may be organized like this:

```text
fusion_demo_notebooks/
├── fusion_demo.ipynb
└── datasets/
    └── Dataset_Name/
        ├── ometiff-pyramids/
        ├── Segmented_FTU/
        ├── Aggregated_FTU/
        └── Files/
```

The exact folder contents may vary depending on which notebook sections and analysis jobs are run.

## Notes for Users

* Run the notebook cells in order.
* If the notebook asks for FUSION credentials, use your FUSION Platform login.
* If you restart the notebook kernel, rerun the authentication cell.

## Exercises

These exercises are designed to help users practice the complete FUSION++ notebook workflow.

### Exercise 1: Access the Workspace and Open the Notebook

**Goal:**
Access either the HuBMAP Workspace or HiPerGator environment, open the FUSION++ notebook, and confirm that FUSION++ is ready to use.

**Tasks:**

1. Access one of the supported workspace environments (HuBMAP/HiperGator).
2. Set up and open the FUSION++ notebook using the instructions above.
3. Select the correct notebook kernel if required.
4. Run the initial setup and authentication cells.
5. Confirm that FUSION++ imports successfully.

**Expected outcome:**
The notebook opens successfully and the initial setup cells run without errors.

---

### Exercise 2: Import Data and Run the Complete Visium Pipeline

**Goal:**
Use data from HuBMAP or FUSION and run the complete Visium pipeline in the notebook.

**Tasks:**

1. Select a dataset from either HuBMAP or FUSION.
2. Import and prepare the selected data inside the notebook workspace.
3. Run the Data Management section.
4. Run the complete Visium analysis workflow.
5. Confirm that the expected output files and folders are generated.

**Expected outcome:**
The selected dataset is processed successfully, and the pipeline generates output files for visualization and downstream analysis.

---

### Exercise 3: Create Plots and Interpret Pipeline Outputs

**Goal:**
Use the pipeline outputs to create your own plots and identify interesting patterns or insights.

**Tasks:**

1. Locate the output files generated by the pipeline.
2. Use the outputs to create custom plots using the generated results.
3. Add appropriate titles, labels, and legends.
4. Write a short interpretation for each plot.
5. Summarize at least two interesting insights from the results.

**Expected outcome:**
Custom plots are created from the pipeline outputs, and the user provides a brief interpretation of the observed results.
