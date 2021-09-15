# Capstone-Project


## Pathology-MRI Registration for Improved Prostate MRI

#### Background: 
Prostate cancer is the most common non-cutaneous cancer and second leading cause of death among men in the United States. The American Cancer Society estimates that about 191,930 new cases and about 33,330 deaths from prostate cancer in the United States for 2020. Multi-Parametric Magnetic Resonance Imaging (Mp-MRI) is traditionally used for all aspects of prostate cancer diagnosis such as localization, staging, active surveillance, and recurrence monitoring. However, a leading study indicates that 15-30% of clinically significant cancers are missed by the most-experienced radiologists in the field. There has been much interest in the multimodal co-registration of prostate mp-MRI with other imaging modalities such as computed tomography (CT) for treatment planning, ultrasound for guiding biopsies, and pathology for validation of cancer detection. Each combination of images makes analyzing images from different modalities and sequences, and translating to one another efficiently, thus increasing diagnostic performance.


#### Registration Model: 
In this research work, we developed a registration model, which co-registered pathology image with MRI using SimpleITK, an image analysis toolkit in Python. Three sets of images (histology-apex:MRI, histology-mid: MRI, and histology-base: MRI) of 10 patients (Data source: The Department of Radiology at The University of Chicago Medicine Center) were used.  The registration model has typically two input images: moving (histology) and fixed image (corresponding MRI), and 4 components: an interpolator, a metric, an optimizer, and a transform. The virtual image is the final output of registration, whereby a moving histology image is mapped onto the MRI cross-sectional slice. 

#### Results: 
The initial registration process resulted in the registration grand mean error of 10.6 mm before tuning the registration parameters. The post-registration error dropped nearly 30% to 7.5 mm after tuning the registration parameters.  The registration results have been compared and validated using 3D Slicer, a free image analysis software where same 2D rigid registration is achievable. The grand average Mutual Information (MI) value was 0.51 with a standard deviation of 0.12, which outperformed the 3D Slicer Tool results of 0.42 and a standard deviation of 0.1. 

#### Conclusion:
##### Our pathology MRI registration model with SimpleITK demonstrated the alignment of histopathology slices and their corresponding MRIs which enabled the accurate mapping of histology onto MRI. 
------------------------------------------------------------------------------------------------------------------
This collaborative capstone project is completed by Joseph Costello and S M Nazarat Hossain under supervision of Utku Pamuksuz, PhD. 
