# Build Now – Palantir for Hospitals Recruiting Competition
Palantir technology powers mission-critical, real-world decisions across industries, helping operators to prevent wildfires, distribute vaccines, staff nurses, improve road safety, and more. Build the future with us. Now. 

Our customers come to us with a hunch that the only way to improve their hospital operations, provide the best care, structure effective healthcare policies, or deliver healthcare to more patients is to make better use of their data. The Palantir for Hospitals team is responsible for turning that hunch into reality. 

### Setting Up Your Environment & Submissions
1. Please follow the steps outlined on [the competition homepage](https://palantir.events/buildnow) to set up your AIP Now access.
2. [Get Familiar with AIPNow](/info/aip_now_help.md)
3. [Setup your Project](/info/setup_your_project.md)

**Complete your submission by emailing a sub-two minute video of your demo to [build-now@palantir.com](mailto:build-now@palantir.com) when complete so we can evaluate your work. Please use `LASTNAME_FIRSTNAME_BUILDNOW_SUBMISSION` in the subject line. In your video, show how you approached the prompt, why you chose to manipulate the data in the way you did, who your users are, and the impact you expect this workflow to drive. Submissions are due no later than Friday, October 18th, 2024 and will be evaluated on a rolling basis.** 

### Example Prompts
- Given a patient's notes, how do we generate verifiable diagnoses and highlight concerns/abnormalities for clinicians?
- Create a simulation model that predicts hospital admission rates based on the frequency and types of ICD-10 codes in patient notes over time.
- Use NLP to extract medication names and dosages from patient notes and correlate them with ICD-10 codes to identify potential unsafe drug interactions or contraindications.
- Analyze patterns of healthcare utilization by integrating patient demographics, notes, and ICD-10 codes to model healthcare costs and identify drivers of high expenditures.

You might think you're lacking enough direction to confidently get started, but that's the point. The best solutions can be found by getting your hands dirty and finding out for yourself what could be valuable to solve. The above prompts are just examples of possible paths that *might* make sense. This is meant to be an exercise in exploring a new environment, as much as it is one where you can show off your technical, communication, and decomp skills.

### Link to Data
[Data Extract tar File](https://github.com/JoshWeiner/zelus-palantir-hospitals/raw/main/data/extract.tar.gz?download=) 

This data includes a notional patient notes `PMC_Patient_clean.csv` dataset, and ICD-10 codes, description, and vector embedding dataset `icd_10_codes.csv`.

The PMC_Patient_clean dataset was cleaned and sourced from the following:

> **Zhao, Z., Jin, Q., Chen, F., Peng, T., & Yu, S. (2022).** A Large-scale Dataset of Patient Summaries and Relations for Benchmarking Retrieval-based Clinical Decision Support Systems. Retrieved from [https://arxiv.org/pdf/2202.13876](https://arxiv.org/pdf/2202.13876)

#### Data Documentation

**Dataset 1: PMC_Patient_clean.csv**

| **Field Name** | **Description**                     | **Data Type** |
|----------------|-------------------------------------|---------------|
| `patient_id`   | A continuous id of patients, starting from 0  | Integer        |
| `patient_uid` | Unique ID for each patient, with format PMID-x, where PMID is the PubMed Identifier of the source article of the patient and x denotes index of the patient in source article  | String          |
| `patient_note`    | Summary of patient: symptoms, diagnoses, history, and/or treatment               | String        |
| `age`          | Age of the patient in years              | Integer       |
| `gender`       | Gender of the patient 'M' or 'F'. Male or Female | String        |

**Dataset 2: icd_10_codes.csv**

| **Field Name** | **Description**                     | **Data Type** |
|----------------|-------------------------------------|---------------|
| `icd_10_code`   | CDC/CMS ICD-10 code        | String        |
| `description`| ICD-10 code detailed description/diagnosis | String    |
| `embedded_description`  | Vector embedding of ICD-10 code description/diagnosis | String        |
| `category`| General grouping for ICD-10 descriptions | String    |


[Further Data Documentation](https://github.com/pmc-patients/pmc-patients)

<hr>

[Who am I?](https://en.wikipedia.org/wiki/Zelus)
