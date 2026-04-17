# Azure_TextAnalytics_NLP_project

This project demonstrates core Azure AI Language text analytics capabilities over an `ABC Bank` sample email scenario.

## Purpose And Objectives

- Provision or reuse an Azure AI Language resource
- Save endpoint and key values into a local `.env`
- Run separate notebooks for PII detection, key phrase extraction, named entity recognition, and sentiment or opinion analysis
- Show how structured outputs can be generated from unstructured customer email content

## Notebook Order

1. `Az_create_Language_Service_resources.ipynb`
2. `Extract_PII_(Personally_Identifiable_Information)_of_Emails_for_ABC_Bank.ipynb`
3. `Key_Phase_Extraction_of_Emails_for_ABC_Bank.ipynb`
4. `Named_Entity_Recognition_of_Emails_for_ABC_Bank.ipynb`
5. `Sentiments_and_Opinions_Analysis_of_Emails_for_ABC_Bank.ipynb`

## Assumptions

- You have permission to create an Azure AI Language resource.
- Azure CLI is installed and authenticated.
- The analysis notebooks use `.env` values such as `AZURE_LANGUAGE_ENDPOINT` and `AZURE_LANGUAGE_KEY`.
- The sample email inputs are demonstration content and should be replaced or expanded for a real dataset.
- The notebooks are designed to be run independently after the setup notebook has completed.

## Requirements

- Python 3
- Jupyter Notebook or JupyterLab
- Azure CLI
- Python packages:
  - `python-dotenv`
  - `pandas`
  - `azure-core`
  - `azure-ai-textanalytics`

## Repeat In A Working Environment

1. Create and activate a Python virtual environment.
2. Install the required packages.
3. Run `az login`.
4. Open `Az_create_Language_Service_resources.ipynb`.
5. Replace placeholder subscription, resource, and location values.
6. Run the setup notebook to create the Language resource and write the `.env` file.
7. Run any of the analysis notebooks depending on the text analytics task you want to reproduce.

Example package install:

```powershell
pip install jupyter python-dotenv pandas azure-core azure-ai-textanalytics
```

## Notes

- Each analysis notebook creates its own `TextAnalyticsClient` and can be rerun independently once the `.env` file is available.
- Secrets and private values were replaced with placeholders for publication.

