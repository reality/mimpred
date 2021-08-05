# Evaluating semantic similarity methods for the comparison of text derived phenotypes and clinical outcome prediction
Here we present an adaptable pipeline for the derivation and comparison of patient phenotypes direct from clinical text, in the form of discharge summaries, test results and clinical notes from the MIMIC-III database. Using semantic similarity of phenotypes, we demonstrate the potential for text-derived phenotype profiles in making diagnosis predictions. 

## Requirements 
### Python and Java 
These notebooks require Python 3 (developed in Python 3.8.6) available [here](https://www.python.org/downloads/), and Jupyter notebook (install instructions [here](https://jupyter.org/install). 
To run Komenti and SML via these notebooks, [Java](https://www.java.com/en/) is required. 
### Semantic Measures Library (SML)
The SML toolkit (.jar) should be available in the working directory, available through their [website](https://www.semantic-measures-library.org/sml/index.php?q=downloads).
### MIMIC-III
To access MIMIC data files, an ethics course must be undertaken. Files can then be downloaded from their [webiste](https://physionet.org/content/mimiciii/1.4/), as detailed in the 'Install and setup' notebook.

## Notebooks
1. **Install and setup**
Relevant downloads, patient sampling and text annotation. Recreate our sample of 1000 patients from MIMIC or create a new sample, extract the text for each patient and apply [Komenti](https://github.com/reality/komenti) to annotate phenotypes. 
2. **Annotation preprocessing**
Extract phenotypes from the annotation and build patient phenotype profiles, in preparation for using the Semantic Measures Library. 
3. **GenerateXML/Generate XML configuration**
Produce custom XML files comprising all available similarity measures through SML (listed in 'measures_revised'), split into IC-based, non-IC based and direct groupwise measures.  
4. **Similarity with SML**
Guidance for running SML in the command line to compare patient phenotypes. 
5. **Results performance**
Evaluation of the similarity measures for predicting primary diagnosis, producing metrics files that can be used for plotting purposes.
6. **Results figures**
Plot ROC curves for individual measures, and histograms of the evaluation metrics across all similarity measures. 


