## Corresponding Kaggle Notebook Link 
https://www.kaggle.com/code/prasundatta/melanoma-classification-data-visualization-eda

## Description

Skin cancer is the most prevalent type of cancer. Melanoma, specifically, is responsible for 75% of skin cancer deaths, despite being the least common skin cancer. The American Cancer Society estimates over 100,000 new melanoma cases will be diagnosed in 2020. It's also expected that almost 7,000 people will die from the disease. As with other cancers, early and accurate detection—potentially aided by data science—can make treatment more effective.

Currently, dermatologists evaluate every one of a patient's moles to identify outlier lesions or “ugly ducklings” that are most likely to be melanoma. Existing AI approaches have not adequately considered this clinical frame of reference. Dermatologists could enhance their diagnostic accuracy if detection algorithms take into account “contextual” images within the same patient to determine which images represent a melanoma. If successful, classifiers would be more accurate and could better support dermatological clinic work.

In this competition, you’ll identify melanoma in images of skin lesions. In particular, you’ll use images within the same patient and determine which are likely to represent a melanoma. Using patient-level contextual information may help the development of image analysis tools, which could better support clinical dermatologists.

Melanoma is a deadly disease, but if caught early, most melanomas can be cured with minor surgery. Image analysis tools that automate the diagnosis of melanoma will improve dermatologists' diagnostic accuracy. Better detection of melanoma has the opportunity to positively impact millions of people.

## Dataset Description

### What files do I need? 
You will need the training and test images, as well as train.csv and test.csv. The images are grouped in directories by study and series. They are in DICOM format, and contain additional metadata that may be relevant to the competition. Each image has a unique identifier - ``` SOPInstanceUID.```

The location for each image is given by: ``` <StudyInstanceUID>/<SeriesInstanceUID>/<SOPInstanceUID>.dcm. ```

The data provided by the host for this competition and made available below is the RSNA-STR PE CT (RSPECT) dataset. Use of the dataset for non-commercial and/or academic purposes is permitted with citation.
### What should I expect the data format to be?
train.csv contains the three UIDs noted above, and a number of labels. Some are targets which require predictions, and some are informational, which will also be noted below in Data fields.
test.csv contains only the three UIDs.

### Files

- <b> train.csv </b> => contains UIDs and all labels.
- <b> test.csv </b> => contains UIDs.

### Data Fields 
- StudyInstanceUID - unique ID for each study (exam) in the data.
- SeriesInstanceUID - unique ID for each series within the study.
- SOPInstanceUID - unique ID for each image within the study (and data).
- pe_present_on_image - image-level, notes whether any form of PE is present on the image.
- negative_exam_for_pe - exam-level, whether there are any images in the study that have PE present.
- qa_motion - informational, indicates whether radiologists noted an issue with motion in the study.
- qa_contrast - informational, indicates whether radiologists noted an issue with contrast in the study.
- flow_artifact - informational
- rv_lv_ratio_gte_1 - exam-level, indicates whether the RV/LV ratio present in the study is >= 1
- rv_lv_ratio_lt_1 - exam-level, indicates whether the RV/LV ratio present in the study is < 1
- leftsided_pe - exam-level, indicates that there is PE present on the left side of the images in the study
- chronic_pe - exam-level, indicates that the PE in the study is chronic
- true_filling_defect_not_pe - informational, indicates a defect that is NOT PE
- rightsided_pe - exam-level, indicates that there is PE present on the right side of the images in the study
- acute_and_chronic_pe - exam-level, indicates that the PE present in the study is both acute AND chronic
- central_pe - exam-level, indicates that there is PE present in the center of the images in the study
- indeterminate -exam-level, indicates that while the study is not negative for PE, an ultimate set of exam-level labels could not be created, due to QA issues






