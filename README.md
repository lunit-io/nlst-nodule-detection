# nlst-nodule-detection

## About The Project

In our study, we evaluated the performance of a commercially available AI algorithm (Lunit INSIGHT for CXR, accessible at https://insight.lunit.io) for nodule detection using the publicly available NLST dataset(https://cdas.cancer.gov/nlst/). 

The NLST dataset consists of anonymized DICOM files of screening chest X-rays, cancer diagnosis and survival information, and NLST radiologists' assessment of the chest X-rays. A more detailed overview and study design can be found in the provided Radiology paper (https://pubs.rsna.org/doi/full/10.1148/radiol.10091808). 

## Preparation of the Nodule Data Set

A subset (n=577) of the patients with available baseline images were selected and annotated for the presence of nodules. The selection process was as belows:

1. CXRs of patients (n=48) with lung cancer diagnosis within 1 year of T0 screening were selected. 
2. CXRs of patients (n=50) with all three screening CXRs and non-calcified nodules (as marked by NLST radiologists), but without a lung cancer diagnosis, were selected.
3. CXRs of patients (n=480) not satisfying the above two criteria were selected
4. CXR that did not contain adequate view of the lung (n=1) was removed from analysis.

##
