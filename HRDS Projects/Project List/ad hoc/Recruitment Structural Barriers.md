
# Columns
|Column                  |dtypes         |Original Column Names                                                                                                                                                                                   |
|:-----------------------|:--------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|id                      |int64          |ID                                                                                                                                                                                                      |
|start_time              |datetime64[ns] |Start time                                                                                                                                                                                              |
|completion_time         |datetime64[ns] |Completion time                                                                                                                                                                                         |
|language                |object         |Language                                                                                                                                                                                                |
|employee_status         |object         |Please select the category that best describes you:                                                                                                                                                     |
|role_type               |object         |Please select the category that best describes your area of work:                                                                                                                                       |
|country                 |object         |Please select your country / region:                                                                                                                                                                    |
|work_location           |object         |Please select your work location (select all that apply):                                                                                                                                               |
|group_function          |object         |Please select your Product Group / Function:                                                                                                                                                            |
|gender                  |object         |Please select your gender:                                                                                                                                                                              |
|age                     |object         |Please select your age category:                                                                                                                                                                        |
|rio_length              |object         |How long have you worked at Rio Tinto?                                                                                                                                                                  |
|minority_identity       |object         |Do you identify with one or more of the following groups that are underrepresented at Rio Tinto?                                                                                                        |
|recruit_length          |object         |How long ago did you experience the Rio Tinto recruitment process?                                                                                                                                      |
|recruit_opportunity     |object         |Was this for a promotional, individual contributor or leadership opportunity?                                                                                                                           |
|successful              |object         |Were you successful in your application?                                                                                                                                                                |
|job_awareness           |float64        |Stage 1: Awareness, visibility, and promotion of the job opportunity?                                                                                                                                   |
|before_interview        |float64        |Stage 2: Applying for the role and before the interview?                                                                                                                                                |
|participating_interview |float64        |Stage 3: Participating in the interview/s?                                                                                                                                                              |
|job_offer               |float64        |Stage 4: Job offer; checks and medicals?                                                                                                                                                                |
|skills_equality         |float64        |Overall, how well did you think the recruitment process explored your skills, knowledge and experience in a way that allowed you to participate equitably for the position?                             |
|unfair_obstacle         |object         |Did you encounter any other obstacles that you believe hindered you from participating fairly for the position?                                                                                         |
|equitable_suggestion    |object         |What suggestions do you have for improving the process at Rio Tinto, in terms of increasing equitability and accessibility or removing obstacles and biases?                                            |
|fair_description        |float64        |How fair and inclusive was the written job description, criteria, and pre-requisites for the role you were applying for?                                                                                |
|description_suggestion  |object         |Do you have any suggestions for how this could be improved?                                                                                                                                             |
|visible_advertisement   |float64        |How easily accessible and visible was the job advertisement for you?                                                                                                                                    |
|leader_support          |float64        |For internal promotion candidates: How supportive was your leader of your job development and advancement?                                                                                              |
|leader_suggestion       |object         |Do you have any suggestions for how they could have been more supportive?                                                                                                                               |
|accessible_tools        |float64        |How accessible and inclusive were the online recruitment and assessment tools (i.e. online psychometrics, desktop, or other assessments) that you were required to use to submit and manage your app... |
|tools_suggestion        |object         |Do you have any suggestions for how these recruitment and assessment tools could be improved?                                                                                                           |
|preinterview_comms      |float64        |How accessible and inclusive was the communication that you received from the Talent Aquisition team during any pre-interview phone conversations and / or emails?                                      |
|comms_suggestion        |object         |Do you have any positive feedback from your communication with the Talent Acquisition team or suggestion on how it could be improved?                                                                   |
|information_safety      |float64        |How safe did you feel about sharing personal information about yourself?                                                                                                                                |
|confidential_confidence |float64        |How confident did you feel that you could trust your personal information would be kept confidential throughout the process?                                                                            |
|withhold_info           |object         |Did you choose to withhold information about yourself to increase your chances of success?                                                                                                              |
|safe_opinions           |float64        |How safe did you feel expressing your opinions and perspectives during the interview process – i.e., being your authentic self?                                                                         |
|comfortable_adjustments |float64        |How comfortable did you feel expressing your needs during or after the interview process, as they relate to flexible work arrangements, reasonable workplace adjustments or other personal needs?       |
|needs_accommodated      |object         |Were your needs accommodated?                                                                                                                                                                           |
|accommodated_explain    |object         |If you selected No to question 35, please provide further context if any attempts to accommodate requests were made.                                                                                    |
|process_suggestion      |object         |Do you have any suggestions for how the interview process can be made more fair, accessible and inclusive?                                                                                              |
|comfortable_checks      |float64        |How comfortable did you feel participating in medicals and other checks?                                                                                                                                |
|fair_offer              |float64        |How satisfied did you feel that the offer presented was fair and equitable and representative of your skill and experience?                                                                             |
|offer_explain           |object         |Why or why not?                                                                                                                                                                                         |
|other_suggestion        |object         |Is there any other specific feedback (positive or other) that you would like to share about your experience as a candidate that would help us to ensure our process is fair, accessible, and inclusi... |
|successful_bin          |int64          |NA                                                                                                                                                                                                      |
|minority_bin            |int64          |NA                                                                                                                                                                                                      |
|internal_bin            |int64          |NA                                                                                                                                                                                                      |
|neurodiverse_identity   |bool           |NA                                                                                                                                                                                                      |
|email                   |NA             |Email                                                                                                                                                                                                   |
|name                    |NA             |Name                                                                                                                                                                                                    |
|participation           |NA             |Please confirm your participation below:                                                                                                                                                                |
# Hypotheses

![[hypotheses 1.png]]

1 A. 

**fair_description** - float64: How fair and inclusive was the written job description, criteria, and pre-requisites for the role you were applying for?|

**description_suggestion** - object: Do you have any suggestions for how this could be improved?

2 A. 

**fair_description**: How fair and inclusive was the written job description, criteria, and pre-requisites for the role you were applying for?|


**accessible_tools:** How accessible and inclusive were the onlineÂ recruitment and assessment tools (i.e. online psychometrics, desktop, or other assessments)Â that you were required to use to submit and manageÂ your app...|

2 B. 

**visible_advertisement* - float64: How easily accessible and visible was the job advertisement for you?

3 A. 

|skills_equality|float64|Overall, how well did you think the recruitment process explored your skills, knowledge and experience in a way that allowed you to participate equitably for the position?|

3 B. 

|accessible_tools|float64|How accessible and inclusive were the online recruitment and assessment tools (i.e. online psychometrics, desktop, or other assessments) that you were required to use to submit and manage your app...|
