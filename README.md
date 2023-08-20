# Brain Tumor Detection

![health-care-logo-design-concept-care-logo-vector-280002222](https://github.com/EDJR94/brain_tumor_detection/assets/128603807/70070dd6-a9af-48cd-aa3c-2d703dade6bd)

## Business Problem

The hospital named 'HealthCare Center' conducts brain tumor diagnoses on its patients. They currently rely on manual examinations to classify tumors, which can lead to diagnostic errors and treatment delays. The hospital decides to implement a **machine learning model to classify tumors** with high accuracy.

Currently, the hospital has a diagnostic **error rate of 5%** in its brain MRI scan results.

### What is a Brain Tumor?

A brain tumor occurs when abnormal cells form within the brain. There are two main types of tumors: cancerous (malignant) tumors and benign tumors. Cancerous tumors can be divided into primary tumors, which start within the brain, and secondary tumors, which have spread from elsewhere, known as brain metastasis tumors. All types of brain tumors may produce symptoms that vary depending on the part of the brain involved. These symptoms may include headaches, seizures, problems with vision, vomiting and mental changes. The headache is classically worse in the morning and goes away with vomiting. Other symptoms may include difficulty walking, speaking or with sensations. As the disease progresses, unconsciousness may occur.

![image](https://github.com/EDJR94/brain_tumor_detection/assets/128603807/be6e5d52-d988-48ef-bcdb-ddffddbdcc23)


*Brain metastasis in the right cerebral hemisphere from lung cancer, shown on magnetic resonance imaging.*

## Data Description

Our MRI Brain Scans Data contains 253 images (256x256 pixels) divided in 2 classes:

- 155 images of Tumor Brains Scans
- 98 images of Normal Brains Scans

This are some samples for our dataset:

![image](https://github.com/EDJR94/brain_tumor_detection/assets/128603807/fbdb4774-6181-49a9-8c80-f4c3a1f3615d)


## Convolutional Neural Network

A Convolutional Neural Network (CNN) is a specialized type of artificial neural network designed for processing grid-like data, such as images. CNNs are adept at capturing local and hierarchical patterns in data, making them highly effective for image pattern recognition tasks. They utilize convolutional layers to apply filters and extract features from input data, enabling tasks like image classification, object detection, and image segmentation.

After some data preparation and preprocessing the 253 images I used 224 of them for Training and Validation(in this phase the model is learning patterns) and 29 for Testing if my model was able to generalize after it learned, this was the results:

![image](https://github.com/EDJR94/brain_tumor_detection/assets/128603807/1e0a8a4f-9390-4487-b4f0-81e3a2800b05)


In the Test Data we have 12 images of Normal Brains and 17 images of Tumor Brains, the model labeled all of them correctly! So it had a 100% Accuracy!

## Business Performace

Let’s look on how Health Care Hospital can take advantage with this model

First, let's look on how the **tradicional diagnosis** for brain tumors works:

1. **Initial Medical Consultation:** The patient visits a doctor who evaluates their symptoms and medical history. This usually takes about 30 minutes.
2. **Referral for Diagnostic Tests:** Based on the consultation, the doctor may recommend diagnostic tests such as MRI and cerebral angiography. Scheduling and conducting these tests might take several days.
3. **Completion of Diagnostic Tests**: The patient undergoes the recommended tests, which can last around 1 to 2 hours each.
4. **Radiological Analysis:** Specialized radiologists analyze the test results and produce reports for the medical team. This process might take 1 to 3 days, depending on workload.
5. **Medical Discussion and Diagnosis:** Medical professionals review the reports and hold discussions to arrive at a diagnosis. This step can take additional days.
6. **Confirmation through Biopsy (If Needed):** If the diagnosis remains uncertain, a biopsy might be recommended, which requires additional scheduling and procedure time, typically spanning a few weeks.
7. **Final Diagnosis and Treatment Planning:** The medical team consolidates information, makes a final diagnosis, and discusses treatment options with the patient. This could span from several more days to weeks.

**Total Time:** The traditional diagnosis process can take anywhere from a **few weeks to over a month**, influenced by the case complexity and logistical factors.

- Looking at our model, we could greatly decrease the 4th and 5th steps from the tradicional diagnosis, **reducing the diagnosis from several weeks to several hours to a day**.

---

Second, What is the error rate for MRI Scans?

According to [this article](https://pubs.rsna.org/doi/abs/10.1148/rg.2018180021?journalCode=radiographics) from RadioGraphics, the average diagostic error rate ranges from **3% to 5%** involving imaging.

Assuming that the error rate for HealthCare Center is 5% and the hospital serves an average of 200 patients per month for brain tumor examinations and each patient generates an average revenue of $5,000 our financial impacts for HealthCare Center will be:

Lost Revenue due to incorrect diagnoses(5% of 200 patients) = 10 patients x $5,000 = $50,000.

If our model corrects these inaccurate diagnoses for the hospital, the **revenue would increase by $50,000 per month or  $600,000 per year**.

## References

Author: Edilson Santos, Data Scientist

Portfolio: https://edjr94.github.io/portfolio_projetos/

LinkedIn: https://www.linkedin.com/in/edilsonsantosjr/

Dataset: https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection
