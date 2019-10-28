# GPT-2 Fine tuned
This repository contains the links to 3 fine tuned GPT-2 models, the datasets used to train them are available in the /datasets folder.

## World of Warcraft - Quests
Download links available : 
- 335M :
- 117M :

The quests have been processed with the following way:
- Scrap from wowhead.com
- Suppression of all the quests without description
- Suppression of all the quests with the same title & description
- Using RACK in order to get the keywords of the quest

The dataset (Dataset_WoW_quests.txt) use the following tags :
- <|startoftext|> & <|endoftext|> : Indicate start and end of an object (quest)
- <EOK> : Indicate the end of the keyword list
- <EOT> : Indicate the end of the quest's title
- <EOD> : Indicate the end of the quest's description
- <EOP> : Indicate the end of the quest's progress description (ex : "Did you finished ?"), can be False
- <EOA> : Indicate the end of the quest's accomplishment description (ex : "Congratulations !"), can be False
  
Improvments incoming :
- <EOC> : A list of the characters in the quest based on the informations scrapped on WoWPedia
- <EOL> : A list of the locations in the quest based on the informations scrapped on WoWPedia
