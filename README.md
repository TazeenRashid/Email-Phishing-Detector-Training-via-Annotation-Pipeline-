# Email-Phishing-Detector-Training-via-Annotation-Pipeline-
The goal of this project is to work with a real-world sample dataset, get to ground truth and provide that for the ML team, draw conclusions from the data set about sample labeling process, and communicate your findings effectively.
Here is the Dataset.
 
Context
Phishing is a cybercrime where attackers pose as known or trusted entities and contact individuals through email, text or telephone and ask them to share sensitive information. There are many signals that suggest an email is Phishing that need to be used in coordination to accurately identify a Phishing email and often the good ones look remarkably like legitimate and non-malicious emails. Users are often also prompted to enter sensitive data (credit card numbers, bank information, passwords) and this information is used by attackers to access accounts, steal data and identities, and download malware onto the user’s computer.
Accurately detecting Phishing messages is complex for a number of reasons. First, Phishing strategies change and evolve as attackers learn and adjust to defenses. Second, Phishing messages have fuzzy boundaries where a message may or may not be considered Phishing. Third, there are many types of unwanted messages (Phishing, Spam, marketing messages, grey mail) so untrained users are generally poor judges of Phishing messages.
Because of this one of the best methods available is to have highly trained threat analysts labeling if a message is a Phishing attempt (is malicious) or not. Even then there are often cases where even well trained judges disagree. The current data set is one that used real messages that were labeled as malicious or not by a series of three judges. This will be the data set that you use for this take home.
 
Content
This dataset contains 11 features extracted from @7,000 phishing emails and @500,000 legitimate emails, there is no PII or identifying information and it does not include the body text. Three independent judges reviewed and labeled each message as malicious or safe. Missing data is designated as “FALSE”. The 11 features are:
email_ID - A 12 digit alphanumeric identifier for each message.
num_words - Total number of words in the email body
num_unique_words- Count of unique words used
num_stopwords - Count of common stopwords (e.g., "the", "and", "in")
num_links - an approximation of the number of links in the email
num_unique_domains - Number of unique domains in links (e.g., "paypal.com")
num_email_addresses - Count of email addresses found in the text
num_spelling_errors - Count of misspelled words
num_urgent_keywords - Number of urgent words (e.g., "urgent", "verify", "update")
email_date - this is the day the email was received. All emails were received in an approximately two year period
email_time - this is the time of day the email was received
 
The labels are:
label_1 - Target variable: 0 = Safe Email, 1 = Phishing Email
label_2 - Target variable: 0 = Safe Email, 1 = Phishing Email
label_3 - Target variable: 0 = Safe Email, 1 = Phishing Email
 
Objective: Provide the best and most accurate data set for modeling given the labels you have on hand.
 
Existing labeling overview
The labeling for this data set was completed before you were put on the project. There were a series of decisions that were made for cost reasons.
Three judges were used. They were the same three people (i.e., each judge was always the same person).
All malicious cases were judged by at least two judges.
All safe cases were judged by at least one judge. A sample of 20,000 was done by two judges because of cost reasons
A third judge was initially used to resolve disagreements between the first two judges.
At some point in the labeling, the decision was made to have three judges for all cases.
We want to see you do these things
 
Explore and Preprocess the Data
Load and clean the data.
Understand both the labeling data as well as the meta data around the messages (i.e., number of words, urgent words, etc.).
 
Report on the attributes of the labeled data set
Give estimates for the accuracy and reliability of the labelers. What method did you use for this and why did you use that method? What were the alternative methods you considered and why did you decide against them?
Report any issues with the reliability of the judges. What are they and how do they impact the quality of the data set?
Explore if the labeled data is sufficient to build a model. Report on any biases or sampling issues with the labels. If you find any issues, propose and implement a solution to control or correct for that bias.
 
If possible, help set up the machine learning team for success
Get to a final judgement on the label for all messages.
Investigate the relationships between the judgements and each of the independent variables. Put this into an initial report for the ML team
 
Interpret the output of the labeling
Draw conclusions about the labeling from the data you have. Make recommendations for what steps you would take to improve a second round of labeling.
Bonus: Design a labeling task and instructions for the next round of labeling
Given what you have found, design the instructions, sampling techniques, labeling prompts, and optimal labeling team for a new labeled data set that is superior to the current one..
 
What you should document
Create a brief report summarizing:
Your approach
Assumptions made
Results
Challenges encountered
How you would improve the labeling in a second round
What strategy you would use to track the performance of the labeling and the changes you are proposing in the system.
What you should deliver
A final data set that would be provided to the ML/AI team
A document answering the requirements of the exercise
Tables or a report of the labeling and exploratory metrics
What we are evaluating
A good understanding of the quality of the labeling based on an assessment of the data.
The quality of the final data set provided
Your understanding and reporting of the limits of this data set and your decision of how to address those limitations
The viability of the improvements suggested for the second round of labeling
