## Overview of the Project :

Toxic comments disrupt communities, drive users away, and strain moderation efforts. This Toxic Comments empowers moderators to prioritize toxic content for moderation in order to lower their negative impact on the community and decreases the reliance on users flagging comments.

This filter can be used by various social media apps like Facebook, Instagram, Slack, Twitter, etc. so that they can encourage people to look for good things about themselves and their co-workers, resulting in higher levels of well-being. and at the same time inform the people of the injustice and negativity around the world in a healthy manner.

### History behind toxic comment filter :

   Historically, tech companies and their algorithms have struggled with hate speech. In 2016, Microsoft had released a Twitter bot called Tay, whose tweets quickly turned abusive, as it relied on the user responses. Twitter, meanwhile, had a curious case of banning userswho had the phrase ‘Kill me’ in their tweets without knowing the context. And between October 2017 and March 2018, Facebook’s systems were able to filter out only 38 percent of the hate speech posts, made its way to the platform.
   
   Hence, working on understanding the context of a particular word used in a sentence and detecting intentional and unintentional typos is important.

 ### What are toxic comments?
 
  Toxic comments are defined as having at least two of the following properties:
  Abuse: The main goal of the comment is to abuse or offend an individual or group of individuals.
  Trolling: The main goal of the comment is to garner a negative response.
  Lack of contribution: The comment does not actually contribute to the conversation.
  Reasonable reader property: Reading the comment would likely cause a reasonable person to leave a discussion thread.


### MY APPROACH :

   I have used a pretrained BERT for this classification tasks. The overall accuracy is 96.38%. I believe semantic understanding of the comments is very important for filtering out toxic comments and enabling healthy conversations.It found that inserting spaces and making typos reduced the toxicity score drastically. For example if someone introduced a word like ‘love’ in these sentences the score took a plunge. 
   
   I have made the pretraining bert for multi class easier since one has to make a lot of modification to the original script to train a multi class classifier.  So all one needs to do now is to add labels.txt in the data folder to get the classifier running. I have also added a inference script (taking inspiration for the sentiment analysis in the course) for easy testng.

### STEPS TO RUN THE PROJECT :
1. Some general pytorch dependencies:
    `pip install pytorch==0.4.0`

2. To train the classifer :
    You can change the configuration of the classifier using the global_config.yaml in config folder (Details of the configurations can be found in the init function of TrainClassifier) google drive links for dataset https://drive.google.com/drive/folders/1zCz1aU1SrmBEc7Lzb2XZQ7g0hEnpxmgy?usp=sharing and add it in the data folder
    You can train the classifier running the cells of Train_Filter jupyter notebook.
    First time loading may take time since it loads a pretrained model
    
3. To run inference :
    You can change the configuration of the classifier using the global_config.yaml in config folder (Details of the configurations can be found in the init function of Inference) google drive links for trained model : https://drive.google.com/drive/folders/1zCz1aU1SrmBEc7Lzb2XZQ7g0hEnpxmgy?usp=sharing and add it in the model folder
    You can train the classifier running the cells of Run_Prediction jupyter notebook.
    First time loading may take time since it loads a pretrained model
    
### QUICK RESULT :
   You can see the examples output in run_prediction.ipymb
    
