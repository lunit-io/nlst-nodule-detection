## About The Project

In our study, we evaluated the performance of a commercially available AI algorithm (Lunit INSIGHT for CXR, accessible at https://insight.lunit.io) for nodule detection using the publicly available National Lung Screening Trial (NLST) data set. In this repository, *we publicly release the nodule label used in our study.* To download the original DICOM file corresponding to our label, request should be made to CDAS (https://cdas.cancer.gov/).

## Brief Description of NLST 

The NLST was a clinical trial conducted to compare LDCT and standard chest X-ray as screening tools to reduce mortality from lung cancer. The data set consists of anonymized DICOM files of screening chest X-rays, cancer diagnosis and survival information, and NLST radiologists' assessment of the chest X-rays. A more detailed overview and study design of NLST can be found in the Radiology paper (https://pubs.rsna.org/doi/full/10.1148/radiol.10091808). 

## Preparation of the Nodule Data Set

A subset (n=577) of the patients with available baseline images were selected and annotated for the presence of nodules. The selection process was as belows:

1. CXRs of patients (n=48) with lung cancer diagnosis within 1 year of T0 screening were selected. 
2. CXRs of patients (n=50) with all three screening CXRs and non-calcified nodules (as marked by NLST radiologists), but without a lung cancer diagnosis, were selected.
3. CXRs of patients (n=480) not satisfying the above two criteria were selected
4. CXR that did not contain adequate view of the lung (n=1) was removed from analysis.

## Annotation of the Data Set
The nodule data set were labeled by two radiologists (K.H.K., with 6 years of experience, and M. K., with 21 years of experience). 

* Each radiologist independently evaluated T0 CXRs for the presence of non-calcified nodules that are ≥4mm.
* Cancer characteristics as well as all available sequential CXRs for the patient and NLST radiologist labels for the CXRs were provided during annotation.
* A CXR was labeled as positive for non-calcified nodules if the two radiologists agreed on the presence of non-calcified nodules and negative, if otherwise. 
* A CXR was labeled as positive for malignant pulmonary nodules if it was positive for both lung cancer and non-calcified nodules.

## Data Dictionary for public_label.csv
* `cancer_pathology`: whether patient was diagnosed with lung cancer within 1 year of baseline imaging.
* `cancer_time`: time interval from baseline imaging to cancer diagnosis.
* `lesion_size_at_Dx`: size (mm) of the lesion at diagnosis.
* `location_at_Dx`: location of the lesion at diagnosis.
* `stage_at_Dx`: stage of the lesion at diagnosis.
* `is_nodule`: whether the image was labeled as positive for nodule.
* `is_malignant_nodule`: 1 if is_nodule ==1 and cancer_pathology ==1
*  `etc`: miscellaneous notes about the image.

## Contact
Hyunsuk Yoo, Medical Director at Lunit Inc. - hyunsuky@lunit.io

## Disclosure
Hyunsuk Yoo is an employee of Lunit. 
