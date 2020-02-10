---
page_type: sample
languages:
- python
products:
- azureml-sdk
description: "Hands-on labs for content on Microsoft learn"
urlFragment: "https://github.com/MicrosoftDocs/mslearn-aml-labs"
---

# Microsoft Learn - Azure Machine Learning Labs

<!-- 
Guidelines on README format: https://review.docs.microsoft.com/help/onboard/admin/samples/concepts/readme-template?branch=master

Guidance on onboarding samples to docs.microsoft.com/samples: https://review.docs.microsoft.com/help/onboard/admin/samples/process/onboarding?branch=master

Taxonomies for products and languages: https://review.docs.microsoft.com/new-hope/information-architecture/metadata/taxonomies?branch=master
-->

This repository contains the files necessary for hands-on labs to support content on [Microsoft Learn](https://docs.microsoft.com/learn/paths/build-ai-solutions-with-azure-ml-service/).

## Contents

| File/folder       | Description                                |
|-------------------|--------------------------------------------|
| `data`            | Sample data for use in the labs.           |
| `labdocs`         | The lab exercise instructions.             |
| `nn-xxxx_xx.ipynb`| Lab code notebooks                         |
| `.gitignore`      | Define what to ignore at commit time       |
| `CHANGELOG.md`    | List of changes to the labs                |
| `README.md`       | This README file.                          |
| `LICENSE`         | The license for this repo                  |
| `SECURITY.md`     | Security guidance                          |

## Prerequisites

Azure Machine Learning (Azure ML) is a Microsoft Azure-based service for running data science and machine learning workloads at scale in the cloud. To use Azure Machine Learning, you will need an Azure subscription. If you do not already have one, you can sign up for a free trial at [https://azure.microsoft.com](https://azure.microsoft.com).

## Setup

You must follow the instructions in the first lab ([Getting Started with Azure Machine Learning](./labdocs/Lab01.md)) to create an Azure Machine Learning workspace and set up a compute instance to work on before completing any subsequent labs in this repository.

## Completing the Labs

Complete the labs in order by following the links on the [Lab Exercises](./labdocs/README.md) page.

Before completing each lab, we recommend you complete the associated training on [Microsoft Learn](https://docs.microsoft.com/learn/paths/build-ai-solutions-with-azure-ml-service/).
