# GPT-2 Fine tuned
This repository contains the links to 3 fine tuned GPT-2 models, the datasets used to train them are available in the /datasets folder.

## World of Warcraft - Quests
Download links available : 
- 335M :
- 117M :

The quests have been processed with the following way:
- Scraped from wowhead.com
- Suppression of all the quests without description
- Suppression of all the quests with the same title & description
- Using RACK in order to get the keywords of the quest (https://pypi.org/project/python-rack/)

The dataset (Dataset_WoW_quests.txt) use the following tags :
- \<|startoftext|\> & \<|endoftext|\> : Indicate start and end of an object (quest)
- \<EOK\> : Indicate the end of the keyword list
- \<EOT\> : Indicate the end of the quest's title
- \<EOD\> : Indicate the end of the quest's description
- \<EOP\> : Indicate the end of the quest's progress description (ex : "Did you finished ?"), can be False
- \<EOA\> : Indicate the end of the quest's accomplishment description (ex : "Congratulations !"), can be False
  
Improvments incoming :
- \<EOC\> : A list of the characters in the quest based on the informations scrapped on WoWPedia
- \<EOL\> : A list of the locations in the quest based on the informations scrapped on WoWPedia

## SF Short Stories
Download links available :
- 355M :
- 117M : 

The texts have been processed with the following way:
- Scraped from 365tomorrows.com
- Characters & Locations indentification with NeuroNER (https://github.com/Franck-Dernoncourt/NeuroNER)
- Using RACK in order to get the keywords of the text (https://pypi.org/project/python-rack/)

The dataset (Dataset_SF_Short_Stories.txt) use the following tags :
- \<|startoftext|\> & \<|endoftext|\> : Indicate start and end of an object (text)
- \<EOK\> : Indicate the end of the keyword list
- \<EOC\> : Indicate the end of the characters list
- \<EOT\> : Indicate the end of the text's title
