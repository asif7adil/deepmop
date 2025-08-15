<p align="center">
    <em> Advanced Deep Learning Enables Predicition of HSC Mobilization Success </em>
</p>

## Abstract

Hematopoietic stem and progenitor cells (HSPC) transplantation offers a potentially curative therapy for aggressive hematologic malignancies and bone marrow failure syndromes. Effective mobilization of donor CD34+ cells underpins successful HSPC transplantation, yet some healthy donors fail to achieve adequate CD34⁺ yields despite standard granulocyte colony‑stimulating factor (G‑CSF)-based regimens. Early identification of donors who face challenges with mobilization offers opportunities to intervene, and will likely lead to better overall transplantation outcomes and reduced healthcare costs. Here we analyze demographic and pre‑ and post‑G‑CSF laboratory data from 1,160 healthy donors from across multiple institutions, developing two complementary machine‑learning frameworks to predict mobilization outcome. A transformer‑based probabilistic model (TabPFN) trained on baseline complete blood counts (CBCs) rigorously discriminates poor from good mobilizers. Application of the same architecture to donor data after mobilization attains near‑perfect discrimination. To unify the predictive model across time points, we introduce an attention‑aware neural network framework that ingests either baseline or post‑mobilization data via a “lab‑type” context flag, enabling accurate prediction of poor mobilizers both before and after GCSF mobilization. We further validated the enhanced framework on data from over 19,000 healthy donors compiled by the Center for International Blood and Marrow Transplant Research. These interpretable models enable early donor triage and “just-in-time” rescue interventions, providing a data driven foundation for personalized donor mobilization strategies.

## Environment Setup

We will use conda to manage environment. The `environment.yml` file contains the necessary packages.

### Python

We're primarily using Makefile to manage the environment and requirements. The `Makefile` contains the necessary commands to create the environment and install the requirements.

To create the environment, run the following command:

```bash
make create_environment
```

To activate the environment, run the following command:

```bash
conda activate dl_hspc
```

If you need to install a new package, you can either add it to the `environment.yml` file and run the following command:

```bash
make requirements
```

or you can run the following command:

```bash
conda install -n hspc package_name
```

And then record the new package in the `environment.yml` file manually.
