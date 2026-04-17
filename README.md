# azure_AI_automation

This repository contains a set of Azure AI notebook projects that demonstrate how to provision Azure resources, configure notebook environments, and implement common banking-focused AI workflows with sample-safe placeholders.

## Purpose

The repository is intended to show end-to-end Azure AI automation patterns for:

- Azure Custom Vision image classification
- Azure AI Language Conversational Language Understanding (CLU)
- Azure AI Language Custom Question Answering (CQA) with Azure AI Search
- Azure AI Language text analytics tasks such as PII detection, key phrase extraction, named entity recognition, and sentiment analysis

## Project Folders

- `Azure_Custom_Vision_project`: resource setup and image classification workflow
- `Azure_TextAnalytics_CLU_project`: CLU project creation, training, deployment, testing, and reporting
- `Azure_TextAnalytics_CQA_project`: CQA and Azure AI Search setup plus question answering workflow
- `Azure_TextAnalytics_NLP_project`: general text analytics workflows over sample email-style data

## Assumptions

- The notebooks are sanitized for publication. You must replace placeholder values such as subscription IDs, resource names, paths, and dataset locations before running them.
- You have an Azure subscription with permission to create resource groups and Azure AI resources.
- You will run the notebooks in `Python 3` with Jupyter Notebook, JupyterLab, or VS Code notebooks.
- Azure CLI is available for the setup notebooks that create resources and write `.env` files.
- Input datasets such as image folders, FAQ documents, or sample email content are available locally in paths you control.

## Requirements

- Python 3.10+ recommended
- Jupyter Notebook or JupyterLab
- Azure CLI with an authenticated session via `az login`
- A virtual environment tool such as `venv`
- Common Python packages used across the projects:
  - `python-dotenv`
  - `pandas`
  - `matplotlib`
  - `requests`
  - `Pillow`
  - `azure-core`
  - `azure-ai-textanalytics`
  - `azure-ai-language-conversations`
  - `azure-ai-language-questionanswering-authoring`
  - `azure-cognitiveservices-vision-customvision`
  - `msrest`

## Repeat In A Working Environment

1. Create and activate a virtual environment.
2. Install the required Python packages.
3. Sign in to Azure CLI with `az login`.
4. Open the relevant project folder and update any placeholder values, local dataset paths, and resource names.
5. Run the setup notebook for that project first so the required Azure resources and local `.env` entries are created.
6. Run the remaining notebooks in the folder in their intended sequence.

Example setup:

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install jupyter python-dotenv pandas matplotlib requests Pillow azure-core azure-ai-textanalytics azure-ai-language-conversations azure-ai-language-questionanswering-authoring azure-cognitiveservices-vision-customvision msrest
az login
```

## Notes

- Setup notebooks use Azure CLI commands to create or verify resources, fetch keys and endpoints, and write local `.env` files.
- Notebook outputs were cleared before export.
- Secrets, endpoints, identifiers, and private values were replaced with placeholders where needed.

