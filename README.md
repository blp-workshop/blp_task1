# BLP Shared Task 1: Violence Inciting Text Detection (VITD)

In recent times, the pervasive influence of social media has been harnessed by various factions representing diverse religions and backgrounds, unfortunately resulting in a disturbing weaponization of these platforms. Tragically, this has led to the incitement of hatred, which, in turn, has manifested as physical communal violence causing significant loss of life and widespread destruction. The prevalence of communal violence is a longstanding issue that continues to escalate, not only in the Bengal Region, encompassing Bangladesh and the West Bengal Province of India, but also worldwide.

Against this backdrop, it becomes imperative to address and understand the different manifestations of communal violence. To this end, this shared task aims to categorize and discern various forms of communal violence, aiming to shed light on this complex phenomenon and contribute to its mitigation.

## Task Description
This shared task presents a challenge to NLP enthusiasts who wish to participate in a violence inciting text classification task. The  dataset comprises YouTube comments related to the top 10 violent incidents that have occurred in the Bengal region (Bangladesh and West Bengal) within the past 10 years. The dataset encompasses content in Bangla, with comment lengths of up to 600 words. The primary objective of this task is to identify and classify threats associated with violence, which can potentially lead to further incitement of violent acts.

The task categories are defined as follows:

- **Direct Violence**: This category encompasses explicit threats directed towards individuals or communities, including actions such as killing, rape, vandalism, deportation, desocialization (threats urging individuals or communities to abandon their religion, culture, or traditions), and resocialization (threats of forceful conversion). The detection of direct violence is crucial due to its potential to yield severe consequences in the future.

- **Passive Violence**: In this category, instances of violence are represented by the use of derogatory language, abusive remarks, or slang targeting individuals or communities. Additionally, any form of justification for violence is also classified under this category.

- **Non-Violence**: The contents falling under this category pertain to non-violent subjects, such as discussions about social rights or general conversational topics that do not involve any form of violence.

Participants are welcome to build systems for the classification task. The successful completion of this task will contribute significantly to the field of natural language processing and violence detection, facilitating the identification and prevention of potential threats leading to violent incidents.





## Data
### Description
We will provide dataset in CSV format. The dataset contains two columns: "text" and "label". The "text" column contains textual data collected from social media. The values in the "label" column will be 0, 1, or 2, representing different categories of violence.

### Label Definition

| Label             | Category |
| ----------------- | -------- |
| Direct Violence   | 2        |
| Passive Violence  | 1        |
| Non-Violence      | 0        |

### Input data format
Data is currently provided in .csv with train.csv and dev.csv files. A row within the CSV adheres to the following structure:

```
text	label
```
Where:
* text: text
* label: Direct Violence, Passive Violence, Non-Violence

##### Example
```
"ঢাকা কলেজে আগুন লাগিয়ে এই কুলাঙ্গার ছাত্রদের পুরিয়ে মারা উচিৎ,, এরাই এখন গলার কাটা",2
শয়তান মেরে হাসবে না তো কাঁদবে!!,1
যে মারা গেল তার ক্ষতিপূরনের ব‍্যবস্হা করে দেওয়া হোক।,0
```
### Statistics
There are two sets used for training and development purposes. The training set is comprised of 2700 samples, which means it contains 2700 instances of data used to train a machine learning model or algorithm. On the other hand, the development set consists of 1330 samples.
| Dataset | Number of Samples |
| --------| ----------------- |
| Train   |      2700         |
| Dev     |      1330         |

#### Train Set
The training set, which includes 2700 samples, is composed of a diverse range of data. Within this set, approximately 15% of the samples depict direct violence, 34% portray passive violence, and the remaining 51% represent non-violent instances. The following figure shows the percentage distribution in different categories in trainig set.
<div style="text-align:center">
    <img src="\images\train_pie_chart.png" alt="Percentage Distribution in train set: Direct Violence, Passive Violence, Non-Violence">
</div>

#### Development Set
The development set comprises 1330 samples, showcasing a diverse range of data. Among these samples, around 15% illustrate direct violence, 31% depict passive violence, and the remaining 54% represent non-violent instances. The following figure shows the percentage distribution in different categories in development set.
<div style="text-align:center">
    <img src="\images\dev_pie_chart.png" alt="Percentage Distribution in dev set: Direct Violence, Passive Violence, Non-Violence">
</div>

## Important Dates
- **16 July 2023:** Registration on codalab and beginning of the development cycle
- **15 August 2023:** Beginning of the evaluation cycle (test sets release and run submission)
- **18 August 2023:** End of the evaluation cycle
- **20 August 2023:** Publish rank list and share paper submission details
- **12 September 2023:** Deadline for the submission of working notes
- **10 October 2023:** Notification of acceptance
- **18 October 2023:** Camera-ready due
- **8 December 2023:** Workshop co-located with EMNLP (Singapore)

## Competition Link
- [Registration Link](https://docs.google.com/forms/d/175kZhk8Eb5rwMqAifzJ6ULcMt0NVcb1wBl3xaZQe48c/edit?usp=sharing_eil_se_dm&ts=64b19ad0) (Dataset provided after successful registration)
- Contest Link: TBD


## Organizers
- Sourav Saha
- Jahedul Alam Junaed
- Dr. Ruhul Amin, Asst. Professor, Fordham University


## Communication
 - Join us in [Slack](https://join.slack.com/t/blpworkshop/shared_invite/zt-1ryu9eyac-7fevK9A4_Bt~qN_eCK349g) 
 - [Contact the organizers](mailto:violence-inciting-text-detection@googlegroups.com)
## Anti-Harassment Policy
EMNLP adheres to the [ACL Anti-Harassment Policy](https://www.aclweb.org/adminwiki/index.php/Anti-Harassment_Policy). Any participant who experiences harassment or hostile behavior may contact any current member of the [ACL Professional Conduct Committee](https://www.aclweb.org/adminwiki/index.php/Professional_Conduct_Committee). Please be assured that if you approach us, your concerns will be kept in strict confidence, and we will consult with you on any actions taken.
