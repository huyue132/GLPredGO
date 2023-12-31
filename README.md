# GLPredGO: Global-Local Feature Extraction Combined with Multi-source Data to Predict Protein Functions
Proteins, essential components in living organisms, play a crucial role in various fields, including drug development and disease research. With the exponential growth of protein sequences, manual annotation along is insufficient to meet the demands of current research. To enhance the efficiency of protein annotation, several deep learning prediction methods have been developed. However, the variability and complexity of protein data pose challenges in effectively extracting meaningful information and integrating different datasets. In this study, we propose a novel multi-source data approach named GLPredGO that leverages three types of information: protein sequences, structural domains and protein-protein interactions (PPI). There data are analyzed using a feature-independent analysis approach that extracts functional attributes. To accomplish this, we propose two extractors: adaptive local feature extractor (ALE) and dual-scale global-local feature extractor (DSGLE) for extracting sequence and structural domain features. For PPI, we employ a factorization dimensionality reduction method and CNN as feature extractors. Finally, we combine the weighted average method and a multilayer perceptron (which takes into account the weighting relationships between different data) are utilized to cross-fuse the three input features. Experimental results on human datasets shown that GLPredGO outperforms other state-of-the-art methods.

![model](https://raw.githubusercontent.com/huyue132/GLPredGO/main/model.svg)

> ALE obtains overall sequence features by compression units and finer local features of sequences by adaptive convolution, a process that improves the performance of predicting protein functions using only sequences.

>An important advantage of the DSGLE is that the overall attributes of the compressed sequences are taken into account and different local features are obtained through different sizes of receptive fields, thus going beyond homology-based functional prediction.

### requirement:
```text
pytorch==1.12
numpy==1.24.3
tokenizers==0.15
transformers==4.36.2
scikit-learn==1.3.2
python==3.8
pandas==2.0.3
```
