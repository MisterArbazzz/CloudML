# CloudML
Real Time inferencing and deployment of ML models on Microsoft Azure ML

## Overview

This project focuses on setting up an Azure Machine Learning workspace and creating compute targets for running model training and data exploration processes.

## Azure Machine Learning Workspace Setup

To get started with Azure Machine Learning, follow these steps to create a workspace:

1. Sign into the [Microsoft Azure portal](https://portal.azure.com/) using your Microsoft credentials.

2. Select ＋Create a resource, search for Machine Learning, and create a new Machine Learning resource with the following settings:

   - Subscription: Your Azure subscription
   - Resource group: Create or select a resource group
   - Workspace name: Enter a unique name for your workspace
   - Region: Select the geographical region closest to you
   - Storage account: Note the default new storage account that will be created for your workspace
   - Key vault: Note the default new key vault that will be created for your workspace
   - Application insights: Note the default new application insights resource that will be created for your workspace
   - Container registry: None (one will be created automatically the first time you deploy a model to a container)

3. Wait for your workspace to be created (it can take a few minutes). Then go to it in the portal.

4. On the Overview page for your workspace, launch Microsoft Azure Machine Learning Studio (or open a new browser tab and navigate to [https://ml.azure.com](https://ml.azure.com)), and sign into Azure Machine Learning studio using your Microsoft account.

5. In Azure Machine Learning studio, toggle the ☰ icon at the top left to view the various pages in the interface. You can use these pages to manage the resources in your workspace.

## Create Compute Targets

Compute targets are cloud-based resources on which you can run model training and data exploration processes. Follow these steps to create compute targets:

1. In Microsoft Azure Machine Learning studio, navigate to the Compute page under Manage. Here, you can manage the compute targets for your data science activities.

2. Create a new compute instance on the Compute Instances tab with the following settings:

   - Virtual Machine type: CPU
   - Virtual Machine size: Standard_DS11_v2
   - Compute name: enter a unique name
   - Enable SSH access: Unselected

3. While the compute instance is being created, switch to the Compute Clusters tab, and add a new compute cluster with the following settings:

   - Virtual Machine priority: Dedicated
   - Maximum number of nodes: 2
   - Idle seconds before scale down: 120
   - Enable SSH access: Unselected
   - Compute name: enter a unique name
   - Minimum number of nodes: 0
   - Virtual Machine type: CPU
   - Virtual Machine size: Standard_DS11_v2

![img1](https://github.com/MisterArbazzz/CloudML/assets/87564754/3564fc14-3896-4ed6-975e-94a0dc38373a)

![img4](https://github.com/MisterArbazzz/CloudML/assets/87564754/5a386118-1201-48fa-844e-39426ae6c48e)

![img3](https://github.com/MisterArbazzz/CloudML/assets/87564754/8bfa9a7a-dd28-44f7-95fc-f26c215ba290)

![img2](https://github.com/MisterArbazzz/CloudML/assets/87564754/f4173483-3dca-4f5c-b629-300f0f481df3)
