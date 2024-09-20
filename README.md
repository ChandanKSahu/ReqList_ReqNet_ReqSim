# *ReqList*, *ReqNet* and *ReqSim* [![DOI](https://zenodo.org/badge/787057888.svg)](https://zenodo.org/doi/10.5281/zenodo.10976096)

---
> Dataset for the publication:

[**ReqNet and ReqSim: A Network and Semantic Similarity Dataset of Requirements from the Tree Structure of System Requirement Specifications**](https://doi.org/10.1115/1.4065786)

## Abstract

Systems are developed as a solution to the problem space defined by their requirements.
The requirements are acquired during the elicitation process.
The creative nature of the elicitation process, proprietary nature of requirements, the need of extensive preprocessing and the diverse techniques for analysis restricts the development of a requirement dataset. 
There exists no formal or informal method to create a requirement dataset.
Thus, we devise a semi-formal method to create a multi-purpose requirement dataset that harnesses human knowledge in the system requirement specification documents (SyRSDs) to facilitate the deployment of modern computing algorithms.
Our dataset has three forms.
1.  **ReqList**, a list of requirements from $86$ distinct systems with their document structure in pure text form. The $12701$ requirements are ready to leverage natural language processing techniques and unsupervised machine learning techniques.
2. **ReqNet**, a large network of requirements consisting of $17375$ nodes to deploy graph-theoretic algorithms for requirement engineering.
 *ReqNet* portrays small-world network characteristics with an average distance of $\approx 9.5619$ links.
3. **ReqSim**, a dataset consisting of $10933$ pairs of requirements annotated with their similarity scores. *ReqSim* enables sentence-level supervised learning tasks to exploit the semantics of requirements. The similarity scores are coherent with human knowledge.

Our dataset is theoretically grounded by the tree structure of SyRSDs. We devise a method to extract a network from the SyRSDs and mathematically prove that the extracted network is a tree.
The tree structure resonates with the hierarchical nature of the requirement allocation process.

### Graphical Abstract
![image](https://github.com/ChandanKSahu/ReqList_ReqNet_ReqSim/assets/43366602/4c441176-cc76-48ae-90e5-53f88dce5228)

## Citation Information

If you find this dataset useful, please cite:
```
@article{10.1115/1.4065786,
    author = {Sahu, Chandan Kumar and Rai, Rahul and Wiecek, Margaret and Gorsich, David},
    title = "{ReqNet and ReqSim: A Network and Semantic Similarity Dataset of Requirements from the Tree Structure of System Requirement Specifications}",
    journal = {Journal of Computing and Information Science in Engineering},
    pages = {1-15},
    year = {2024},
    month = {06},
    issn = {1530-9827},
    doi = {10.1115/1.4065786},
    url = {https://doi.org/10.1115/1.4065786},
}
```
#### Acknowledgement
We thank the authors of *PURE: A Dataset of Public Requirements Documents* for making their dataset publicly available.
