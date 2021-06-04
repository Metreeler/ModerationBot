# ModerationBot
Bot discord conçu pour l'animation d'atelier de modération.
## Matériel nééssaire au bon fonctionnnement du bot
- Un serveur discord correctement configuré
![Frame 7](https://user-images.githubusercontent.com/85356491/120828148-79705480-c55c-11eb-8ba6-2c94517e821d.png)
*configuration conseillée : un channel textuel par participant + un channel textuel commun + un channel de configuration* 


- Une base de donnée en entrée et en sortie (JSON)  
*par défault la base de donnée en sortie est structurée de la manière suivante :*  
`{
    "message": "message",
    "emoji": "👍",
    "participant": "IDduParticipant"
  },`  
*La base de donnée data.json a été constitué à partir de commentaire collectés sur https://www.bodyguard.ai, elle regroupe donc des commentaires pré-modérés issuent de Twitter, Youtube, Twitch... libre à vous de constituer une autre base de donnée*

-Le "ModerationBot" installé sur votre serveur avec tous les droits administrateurs  
*Le bot doit à minima pouvoir écrire et supprimer des messages dans tous les channels. Il doit également pouvoir réagir à des messages et supprimer des réactions*  

## Structuration d'un atelier

## Les commande du bot 
*les commandes doivent être écrite et envoyée dans le channel paramétrage*
- la commande **start**,lance l'étape sélectionnée.
- La variable **etapeAtelier** détermine l'étape sélectionnée.  
`if(etapeAtelier == 1){
//////////////////// code de la première phase
}else if(etapeAtelier == 2){
//////////////////// code de la phase 2
}else if(etapeAtelier == 3){
//////////////////// code de la phase 3
}`  
A tout moment la commende **atelier1 / aterlier2....** permet de changer la valeur de cette variable et donc de sélectionner une autre étape de l'atelier.
- la commande **end**, cloture l'atelier et assigne à la varible etapeAtelier la valeur "1".
