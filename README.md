# Fair Exercises — Reproducible Workflow

This repository contains a reproducible data analysis workflow developed as part of an exercise on workflows and FAIR principles.

The workflow is implemented as a Jupyter notebook and demonstrates how a computational analysis can be documented, reproduced, and shared with others.

## Repository contents

* `project.ipynb` — Jupyter notebook containing the analysis, explanations, code, and generated outputs.
* `environment.yml` — Conda environment specifying the software dependencies and their versions.
* `LICENSE` — MIT License.

## Requirements

The workflow requires:

* Python
* Conda or Miniconda
* Jupyter Notebook/JupyterLab

The required Python packages and their versions are specified in `environment.yml`.

## Installation

Clone the repository:

```bash
git clone https://github.com/Lukeking01/Fair_exercises.git
cd Fair_exercises
```

Create the Conda environment:

```bash
conda env create -f environment.yml
```

## Running the workflow

Activate the environment:

```bash
conda activate Fair
```

Start Jupyter:

```bash
jupyter notebook
```

Open `project.ipynb` and run the notebook from beginning to end.


## Reproducibility and version pinning

The workflow uses a Conda environment file to specify the software required to run the analysis. Versions of the main dependencies are pinned to reduce the possibility that future package updates change the behaviour of the workflow.

Version pinning is particularly important for scientific Python packages because changes in package APIs, numerical implementations, or dependency requirements can cause previously working code to produce different results or fail to execute.

The environment file therefore provides a documented software environment that can be recreated by other users.

### Risk assessment

Version pinning improves reproducibility but also introduces some long-term risks. Pinned package versions may eventually become outdated, unsupported, or unavailable from package repositories. In addition, dependencies can contain platform-specific components, meaning that an environment created on one operating system may not be completely identical on another.

Future maintenance of the workflow should therefore include testing the notebook with newer package versions and updating `environment.yml` when necessary. The notebook should be rerun after dependency updates to verify that the results and functionality remain correct.

## FAIR principles

The workflow is designed with the FAIR principles in mind:

* **Findable:** The workflow is stored in a public GitHub repository with a descriptive repository name, README, and metadata.
* **Accessible:** The notebook and supporting files can be accessed through GitHub and downloaded or cloned without requiring special access.
* **Interoperable:** The analysis uses widely adopted formats such as Jupyter notebooks, Markdown, Python, and YAML. The Conda environment file provides a machine-readable description of the software dependencies.
* **Reusable:** The workflow contains explanatory text, documented dependencies, executable code, generated outputs, and an open-source license. These components make it easier for another person to understand, reproduce, modify, and extend the analysis.

## License

This project is released under the MIT License. See `LICENSE` for details.

## Keywords

FAIR principles, reproducible research, scientific workflow, Jupyter Notebook, Python, Conda, data analysis, reproducibility
