## Group memebers
Ashley Cagir:blossom:, Jiao Li:cherry_blossom:, Timeka Mister:palm_tree:

## Audience
U.S. Adults suffering from mental health issues due to COVID

## Problem and need
* The COVID-19 pandemic may have brought many changes to how people live, and with it, at times, uncertainty, altered daily routines, financial pressures and social isolation. People may worry about getting sick, how long the pandemic will last, whether our job will be affected and what the future will bring. Information overload, rumors and misinformation can make our life feel out of control and make it unclear what to do.
* During the COVID-19 pandemic, we may experience stress, anxiety, fear, sadness and loneliness, and mental health disorders, including anxiety and depression, can worsen.
* Surveys show a major increase in the number of U.S. adults who report symptoms of stress, anxiety, depression and insomnia during the pandemic, compared with surveys before the pandemic. Some people have increased their use of alcohol or drugs, thinking that can help them cope with their fears about the pandemic. In reality, using these substances can worsen anxiety and depression.
* For all of these reasons, it's important to manage our own mental health and get the care when needed.
* Studies show that aerobic exercise can be used to improve mental health (e.g., anxiety). We want to use this concept to help improve people`s mental health due to COVID.

## Objective/ Scope of this project
* Building a patient-facing application which can monitor a patient’s exercise and mental health level, and potentially improve mental health by exercise intervention and behavior change. 
* Building a physician/caregiver-facing application which can assist the physician/caregiver to understand the patient’s situation and intervenes accordingly.

## Desired features
:iphone: Patient-facing application
* Record PHR
  * Vital signs (heart rate, heart rate variability, skin temperature, etc.) from Apple watch
  * Aerobic exercise data (steps, etc.) from Apple watch and smartphone apps (Apple Health App, Fitbit App, etc.). Record time period and Date Time.
  * Depression questionnaire response (PHQ-9). Ask questionnaire once per day, at evening
* Show PHR
  * Vital signs and exercise trend
  * Depression severity score
* Notification
  * Send a notification to patient when vital is too low (nice to have)

:hospital: Physician/caregiver-facing application
* Show the above PHR in EHR systems
* Send a notification to physician/caregiver when depression level reaches the pre-setting threshold (nice to have)
* Intervene (Care Plan, etc.) via application when PHQ-9 score is too below (nice to have)

:closed_lock_with_key: Authentication

## Relevant data in FHIR
| Data Element | HL7 FHIR Resource | Description |
| --- | --- | --- |
| Patient demographic | Patient | Person who plays the patient role (e.g., age, address, gender) |
| Physician | Practitioner | Person who plays the role of physician, caregiver, etc. |
| Care team | CareTeam | Group of practitioners responsible for patient monitoring |
| Patient location | Location | Location of the patient |
| Patient symptom | Condition | Persistent patient symptoms that need long term management |
| Vital sign | Observation | Vital signs such as blood pressure |
| Body site of sensor | BodySite | Describe sensor place on body |
| Exercise | Procedure | A procedure done by patient as a part of treatment plan |
| Questionnaire | QuestionnaireResponse | A structured set of questions and their answers |

## Will it be embedded or freestanding?
Freestanding

## Will it store custom data? Where?
No custom data storage. Just API connection, including pushing vital signs, exercise data and mental health questionnaire data from patient devices to hospital EHR server and FHIR server, and pulling those data from EHR server and FHIR server to EHR client and patient client.
