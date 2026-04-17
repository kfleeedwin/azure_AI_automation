# Azure_Custom_Vision_project

This project demonstrates how to provision Azure Custom Vision resources and build an image classification workflow for an `ABC Bank` sample use case.

## Purpose And Objectives

- Create or reuse Azure Custom Vision training and prediction resources
- Retrieve endpoints, keys, and resource identifiers needed by the notebooks
- Train and publish an image classification model
- Run predictions against test images to validate the workflow

## Notebook Order

1. `Az_create_Custom_Vision_resources.ipynb`
2. `Image_classification_for_ABC_Bank.ipynb`

## Assumptions

- You have permission to create `CustomVision.Training` and `CustomVision.Prediction` resources in Azure.
- Azure CLI is installed and authenticated.
- The local image dataset paths referenced in the notebook are placeholders and must be updated to match your machine.
- The project uses environment values such as `VISION_TRAINING_ENDPOINT`, `VISION_PREDICTION_ENDPOINT`, `VISION_TRAINING_KEY`, `VISION_PREDICTION_KEY`, and `VISION_PREDICTION_RESOURCE_ID`.
- The example project and publish iteration names can be changed to suit your environment.

## Requirements

- Python 3
- Jupyter Notebook or JupyterLab
- Azure CLI
- Python packages:
  - `python-dotenv`
  - `Pillow`
  - `azure-cognitiveservices-vision-customvision`
  - `msrest`
  - `ipython`

## Repeat In A Working Environment

1. Create and activate a Python virtual environment.
2. Install the required packages.
3. Run `az login`.
4. Open `Az_create_Custom_Vision_resources.ipynb`.
5. Replace placeholder values such as subscription ID, resource group, resource names, and location.
6. Run the setup notebook to create resources and populate the notebook session or `.env` values.
7. Update dataset paths in `Image_classification_for_ABC_Bank.ipynb`.
8. Run the classification notebook to create the project, upload training images, train, publish, and test the model.

Example package install:

```powershell
pip install jupyter python-dotenv Pillow azure-cognitiveservices-vision-customvision msrest ipython
```

## Notes

- The setup notebook uses Azure CLI calls to create resources and fetch keys and endpoints.
- The classification notebook expects local training and test image folders to exist before execution.
- Secrets and private values were replaced with placeholders for publication.

