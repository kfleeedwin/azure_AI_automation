# Azure_TextAnalytics_CLU_project

This project demonstrates a Conversational Language Understanding workflow for an `ABC Bank` customer service scenario, from Azure resource setup through training, deployment, evaluation, and reporting.

## Purpose And Objectives

- Provision or reuse an Azure AI Language resource for CLU
- Create a CLU project and import labeled conversational training data
- Train a model and store project settings in a local `.env`
- Deploy the trained model and test it with sample utterances
- Evaluate results and generate summary artifacts for reporting

## Notebook Order

1. `Azure_Language_CLU_Setup.ipynb`
2. `ABC_Bank_CLU_Create_And_Train.ipynb`
3. `ABC_Bank_CLU_Deploy_And_Test.ipynb`
4. `ABC_Bank_CLU_Evaluate_Results.ipynb`
5. `ABC_Bank_CLU_Report.ipynb`

## Assumptions

- You have an Azure subscription with permission to create an Azure AI Language resource.
- Azure CLI is installed and authenticated.
- The CLU notebooks rely on `.env` values such as `AZURE_LANGUAGE_ENDPOINT`, `AZURE_LANGUAGE_KEY`, `AZURE_CLU_PROJECT_NAME`, `AZURE_CLU_PROJECT_LANGUAGE`, and `AZURE_CLU_MODEL_LABEL`.
- The sample intent and utterance data in the training notebook is a demonstration dataset and should be adapted for real use.
- The reporting notebooks expect evaluation outputs to exist in `analysis_output`.

## Requirements

- Python 3
- Jupyter Notebook or JupyterLab
- Azure CLI
- Python packages:
  - `python-dotenv`
  - `pandas`
  - `matplotlib`
  - `requests`
  - `azure-core`
  - `azure-ai-language-conversations`

## Repeat In A Working Environment

1. Create and activate a Python virtual environment.
2. Install the required packages.
3. Run `az login`.
4. Open `Azure_Language_CLU_Setup.ipynb` and replace placeholder subscription, resource, and location values.
5. Run the setup notebook to create the Azure AI Language resource and write the base `.env` file.
6. Run `ABC_Bank_CLU_Create_And_Train.ipynb` to create the CLU project, import training assets, and train a model.
7. Run `ABC_Bank_CLU_Deploy_And_Test.ipynb` to deploy the model and capture test results.
8. Run `ABC_Bank_CLU_Evaluate_Results.ipynb` and `ABC_Bank_CLU_Report.ipynb` to generate analysis files and reporting outputs.

Example package install:

```powershell
pip install jupyter python-dotenv pandas matplotlib requests azure-core azure-ai-language-conversations
```

## Outputs

- `analysis_output` contains generated evaluation files such as detailed results, summaries, failed cases, and report pack assets.

## Notes

- The training notebook uses the Azure authoring client and preview export format for CLU project assets.
- The evaluation and report notebooks depend on prior execution of the deployment and testing steps.
- Secrets and private values were replaced with placeholders for publication.

