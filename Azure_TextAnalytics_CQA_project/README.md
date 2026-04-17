# Azure_TextAnalytics_CQA_project

This project demonstrates how to set up Azure AI Language and Azure AI Search for a Custom Question Answering solution using an `ABC Bank` FAQ-style knowledge source.

## Purpose And Objectives

- Provision Azure AI Language and Azure AI Search resources
- Write required endpoints, keys, and service names into a local `.env`
- Create or reuse a Custom Question Answering project
- Load source content, add QnA pairs, deploy the project, and test question answering behavior

## Notebook Order

1. `Azure_Language_CQA_and_Search_Setup.ipynb`
2. `Question_Answering_Solution_for_ABC_Bank.ipynb`

## Assumptions

- You have permission to create Azure AI Language and Azure AI Search resources.
- Azure CLI is installed and authenticated.
- The notebooks depend on `.env` values such as `AZURE_LANGUAGE_CQA_ENDPOINT`, `AZURE_LANGUAGE_CQA_KEY`, and Azure AI Search configuration values created by the setup notebook.
- The FAQ document path used in the notebook is a local placeholder and must be updated before execution.
- Search service SKU and region availability may vary by subscription.

## Requirements

- Python 3
- Jupyter Notebook or JupyterLab
- Azure CLI
- Python packages:
  - `python-dotenv`
  - `requests`
  - `azure-core`
  - `azure-ai-language-questionanswering-authoring`

## Repeat In A Working Environment

1. Create and activate a Python virtual environment.
2. Install the required packages.
3. Run `az login`.
4. Open `Azure_Language_CQA_and_Search_Setup.ipynb`.
5. Replace placeholder subscription ID, resource names, location, and SKU values.
6. Run the setup notebook to create the Language and Search resources and write the `.env` file.
7. Update the source document path and project names in `Question_Answering_Solution_for_ABC_Bank.ipynb`.
8. Run the question answering notebook to create the project, ingest source material, deploy it, and test queries.

Example package install:

```powershell
pip install jupyter python-dotenv requests azure-core azure-ai-language-questionanswering-authoring
```

## Notes

- Azure AI Search is a dependency for this workflow, so the setup notebook provisions both services together.
- The authoring notebook includes logic to skip duplicate sources and QnA entries when rerun.
- Secrets and private values were replaced with placeholders for publication.

