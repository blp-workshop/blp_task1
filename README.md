# BLP Shared Task 1: Violence Inciting Text Detection (VITD)

In recent times, the pervasive influence of social media has been harnessed by various factions representing diverse religions and backgrounds, unfortunately resulting in a disturbing weaponization of these platforms. Tragically, this has led to the incitement of hatred, which, in turn, has manifested as physical communal violence causing significant loss of life and widespread destruction. The prevalence of communal violence is a longstanding issue that continues to escalate, not only in the Bengal Region, encompassing Bangladesh and the West Bengal Province of India, but also worldwide.

Against this backdrop, it becomes imperative to address and understand the different manifestations of communal violence. To this end, this shared task aims to categorize and discern various forms of communal violence, aiming to shed light on this complex phenomenon and contribute to its mitigation.

## Task Description
This shared task presents a challenge to NLP enthusiasts who wish to participate in a violence inciting text classification task. The  dataset comprises YouTube comments related to the top 9 violent incidents that have occurred in the Bengal region (Bangladesh and West Bengal) within the past 10 years. The dataset encompasses content in Bangla, with comment lengths of up to 600 words. The primary objective of this task is to identify and classify threats associated with violence, which can potentially lead to further incitement of violent acts.

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

## Baselines

We have used baseline system that fine-tunes the XLM-RoBERTa base model and BERT multilingual base model (cased) for the dataset.

The baseline results for the task on development set are provided in the below table.

| Model                             | macro-F1 |
|-----------------------------------|----------|
| BanglaBERT    		            | 0.7879   |
| XLM-RoBERTa base                  | 0.7292   |
| BERT multilingual base (cased)    | 0.6819   |


## Important Dates
- **16 July 2023:** Registration on codalab and beginning of the development cycle
- **15 August 2023:** Beginning of the evaluation cycle (test sets release and run submission)
- **18 August 2023:** End of the evaluation cycle
- **20 August 2023:** Publish rank list and share paper submission details
- **10 September 2023:** Deadline for the submission of working notes
- **10 October 2023:** Notification of acceptance
- **16 October 2023:** Camera-ready due
- **8 December 2023:** Workshop co-located with EMNLP (Singapore)

## Competition 
- [Dataset of Trial Phase](https://docs.google.com/forms/d/175kZhk8Eb5rwMqAifzJ6ULcMt0NVcb1wBl3xaZQe48c/edit?usp=sharing_eil_se_dm&ts=64b19ad0) (Dataset provided after successful registration)
- To participate in this competition, you must have an account in [codalab](https://codalab.lisn.upsaclay.fr/)
- Contest Link: https://codalab.lisn.upsaclay.fr/competitions/14620
- This competition consists of two phases:
    - **Trial Phase:** This phase involves working on the dev set.
    - **Evaluation Phase:** This phase involves working on the test set, which will be released during the evaluation cycle.
- Participants can form a team with multiple people or a single-person team is okay.
- We request each team to establish and manage a single account for all submissions. Any submissions made from multiple accounts by the same team may lead to your system being not ranked from the final ranking in the overview paper.
- Your best score will automatically be added to the leaderboard and it will serve as your final submission. 
- Each team is allowed a maximum of 30 submissions per day for the given task.
- [Team Registration Form](https://docs.google.com/forms/d/1EeyN90p_icJI9DIorv1JGqx83Q9u2qPPhRK51vVjS_I/edit?ts=64d87b0d) - Hit the link and fill out this form (Test set for evaluation phase provided after successful registration)


## Submission Guidelines
Your submissions will be evaluated by macro F1 comparing with the ground truth. The leaderboard’s performance is ranked by macro-F1 in descending order. To check more detailed evaluation scores after submission, you can "View scoring output log".
### Format of Prediction File
The prediction file should follow the CSV format. In the CSV file, there should have exactly two columns named "text" and "label". The "label" column will be used for evaluation. The values in the "label" column should range from 0 to 2, as there are three classes in our task. In the prediction file, the order of the data should be the order given by us. We have provided sample prediction files below for your convenience.
- [Sample prediction file for trial phase](https://drive.google.com/file/d/13mRoMGscsVmHhd5M-pJfDFMxJzSMDmiV/view?usp=sharing)
- [Sample prediction file for evaluation phase](https://drive.google.com/file/d/1xsUwrxiRZ7oqCqn1pguGUtC3qZ1fr7Vz/view?usp=sharing)
### Prepare Submission Files
Follow the instructions below to submit your prediction file. Codalab requires all submissions to be in zip format.
<ul>
	<li>Use your trained model to generate a prediction file.</li>
	<li>Name the prediction file in the format of <code>&lt;file_name&gt;.csv</code>, where <code>&lt;file_name&gt;</code> represents a descriptive name of your choice.</li>
	<li>Compress the <code>&lt;file_name&gt;.csv</code> file into a zip file.</li>
	<li>Submit the zip file on Codalab.</li>
</ul>
After a successful submission, you need to click the <b>Submit to Leaderboard</b> button to submit the score to the leaderboard.

## Rank List 
| Rank | Team Name            | Affiliation                                           | Username          | Submission Id|F1 Score (Macro) |
|------|----------------------|-------------------------------------------------------|-------------------|--------|------------------|
| 1    | DeepBlueAI           | DeepBlue Technology (Shanghai) Co., Ltd               | DeepBlueAI        |520420 |76.044            |
| 2    | Aambela             | CCDS Lab, IUB, Dhaka                                  | MoFa_Aambela      | 520141|76.040            |
| 3    | NLP_CUET             | Chittagong University of Engineering and Technology  | NLP_TEAM          | 520009 |74.587            |
| 4    | Team Embeddings      | NA                                                    | towhidul_tonmoy   | 517629|74.418            |
| 5    | Semantics Squad      | University of New Brunswick                          | KrishnoDey        | 518447|74.413            |
| 6    | nlpBDpatriots      | GEORGE MASON UNIVERSITY                               | Raihan008         | 516557|74.313            |
| 7    | the_linguists        | Islamic University of Technology                    | tariquzzaman      | 516636|73.978            |
| 8    | Panda                | Researcher                                           | yangst            |516283| 73.808            |
| 9    | EmptyMind            | Chittagong University of Engineering and Technology  | empty_box         | 518295| 73.797            |
| 10   | Mavericks            | Pune Institute of Computer Technology               | kshitij           | 520353| 73.699            |
| 11   | LowResourceNLU       | University of California Los Angeles (UCLA), Virginia Tech, James Cook University  | Hari_vm |520336 | 73.468            |
| 12   | VacLM                | IIT Kanpur			                   | pramitb          |516939 | 72.656            |
| 13   | LexicalMinds         | Chittagong University of Engineering and Technology  | saha17         |519925   | 72.551            |
| 14   | Score_IsAll_You_Need | Chittagong University of Engineering and Technology  | Ka05aR          |520135  | 72.376            |
| 15   | winging_it           | Islamic University of Technology                    | shihab16       |517184   | 71.207            |
| 16   | Semantic_Savants     | Chittagong University of Engineering and Technology  | Semantic_Savants |515469 | 71.179            |
| 17   | BpHigh        | Independent                                          | bp-high        |520550   | 70.978            |
| 18   | SUST_Black Box       | Shahjalal University of Science & Technology        | hrithik4064  |520481     | 70.680            |
| 19   | Team_Syrax           | Shahjalal University of Science & Technology        | riyadomf     |520099     | 70.450            |
| 20   | Blue                 | North South University                              | ShadmanRohan  |520323    | 70.012            |
| 21   | Team CentreBack      | Independent                                          | refaat1731    |515685    | 69.390            |
| 22   | Souro                | Charles University                                   | souro    |520101         | 69.009            |
| 23   | BanglaNLP            | Self                                                 | Ssaha    |517168         | 68.110            |
| 24   | KUET_NLP             | Khulna University of Engineering & Technology       | shakib034    |520056     | 60.332            |
| 25   | Shibli_CL            | Ahsanullah University of Science and Technology     | Shibli_CL  |515841       | 38.427            |
| 26   | Ushoshi2023          | Daffodil International University, Florida Institute of Technology, University of North Carolina at Charlotte, United International University | nnur594 |520100| 31.913            |
| 26   | Team Error Point     | Daffodil International University                   | rajeshdiu    |520024     | 31.913            |
| 27   | lixn                 | LMU                                                  | lixn    |520468          | 31.426            |


## Organizers
- Sourav Saha, Shahjalal University of Science and Technology
- Jahedul Alam Junaed, Shahjalal University of Science and Technology
- Dr. Nabeel Mohammed, Associate Professor, North South University
- Dr. Ruhul Amin, Asst. Professor, Fordham University

## Citation
Please use the following BibTeX to cite the dataset and the task.

### Dataset Paper:
```
@inproceedings{SahaAndJunaed,
  title = “Vio-Lens: A Novel Dataset of Annotated Social Network Posts Leading to
Different Forms of Communal Violence and its Evaluation”,
  author= “Saha, Sourav and Junaed, Jahedul Alam  and Api, Arnab Sen Sharma and Mohammad, Nabeel and Amin, Mohammad Ruhul”,
  booktitle =  "Proceedings of the 1st International Workshop on Bangla Language Processing (BLP-2023)”,
  month = “dec”,
  year = ”2023”,
  publisher = "Association for Computational Linguistics",
  address = “Singapore”,
}
```
### Task Description Paper:
```
@inproceedings{blp2023-overview-task1,
  title = “BLP-2023 Task 1: Violence Inciting Text Detection (VITD)”,
  author= “Saha, Sourav and Junaed, Jahedul Alam and Mohammed, Nabeel and Kar, Sudipta and Amin, Mohammad Ruhul”,
  booktitle =  "Proceedings of the 1st International Workshop on Bangla Language Processing (BLP-2023)”,
  month = “dec”,
  year = ”2023”,
  publisher = "Association for Computational Linguistics",
  address = “Singapore”,
}

```



## Communication
 - Join us in [Slack](https://join.slack.com/t/blpworkshop/shared_invite/zt-1ryu9eyac-7fevK9A4_Bt~qN_eCK349g) 
 - [Contact the organizers](mailto:violence-inciting-text-detection@googlegroups.com)
## Anti-Harassment Policy
EMNLP adheres to the [ACL Anti-Harassment Policy](https://www.aclweb.org/adminwiki/index.php/Anti-Harassment_Policy). Any participant who experiences harassment or hostile behavior may contact any current member of the [ACL Professional Conduct Committee](https://www.aclweb.org/adminwiki/index.php/Professional_Conduct_Committee). Please be assured that if you approach us, your concerns will be kept in strict confidence, and we will consult with you on any actions taken.
