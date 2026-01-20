# NORDSTAR-projection
In a previous study, we identified four different RA subsets, characterized mainly by their Joint Involvement Patterns (**JIP**): JIP-foot) arthritis in feet, JIP-oligo) seropositive oligo-articular disease, JIP-hand) seronegative hand arthritis, JIP-poly) polyarthritis.

This github repo concerns a follow-up study, where we cast the NORDSTAR & BeSt trial data onto the patient embedding, to see if these JIPs are also recurrent in this patient population & to see if they show a differential response to different treatment arms/

![alt text](https://github.com/levrex/NORDSTAR-projection/blob/main/figures/md/JIP_projection_NORDSTAR.jpg?raw=true)

For more information on our previous findings, see our article published in npj Digital Medicine: https://www.nature.com/articles/s41746-025-01997-1

[Click here to find the codebase of our initial study](https://github.com/levrex/EHR-Clustering-RA/)


## Installation

#### Windows systems:
Prerequisite: Install [Anaconda](https://www.anaconda.com/distribution/) with python version 3.8+. This additionally installs the Anaconda Prompt, which you can find in the windows search bar. Use this Anaconda prompt to run the commands mentioned below.

#### Linux / Windows (dev) systems:
Prerequisite: [conda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html) environment (with jupyter notebook). Use the terminal to run the commands mentioned below.

#### Install Jupyter Notebook:
```sh
$ conda install -c anaconda notebook
```

#### Install required modules
Use pip to install the dependecies

```sh
$ pip install -r requirements.txt
```


## Directory Structure

* `figures/*`: All figures of the project are stored here
* `models/*`: Here you find the models used to project the novel patients onto the previously learned patient embedding
* `notebooks/*`: Features the notebooks where we do the preprocessing of the data, cluster assignment & analysis
* `notebooks/offshoots/Compare_clustering_ESR_vs_CRP.ipynb*`: We also did a seperate sensitivity analysis to see effect of clustering w/ CRP instead of ESR 
* `src/*`: All python scripts used for preprocessing the data are stored here 
* `umap/*`: The parametric umap is stored here

### Replication in a second dataset
e assigned patients from the JIP dataset to existing clusters by projecting them into the previously established patient embedding space. Using the [POODLE](https://github.com/levrex/Poodle) framework, each new patient’s coordinates were calculated relative to the original latent structure. Patients were then assigned to specific clusters based on their spatial orientation and proximity within this shared embedding. 

## Citation
If you were to use this pipeline, please use the following citation:  

Maarseveen, T.D., Maurits, M.P., Coletto, L.A. et al. Location and amount of joint involvement differentiates rheumatoid arthritis into different clinical subsets. npj Digit. Med. 8, 623 (2025). https://doi.org/10.1038/s41746-025-01997-1 

## Contact
If you experience difficulties with implementing the pipeline or if you have any other questions feel free to send me an e-mail. You can contact me on: t.d.maarseveen@lumc.nl
