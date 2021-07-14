# PrimPopBot

Un chatbot pour https://primairepopulaire.fr/ 

Voir le bot : https://chat.csml.dev/channels/difm7vtdxz0rr16wigcqnk8sbmqkioxi

## Synchronisation GitHub -> CSML

  ### GitHub
  
  * Se créer un compte Github
  * Demander à être ajouter dans le groupe de travail (organisation)
  * Se rendre sur https://github.com/primairepopulaire
  * Créer une nouvelle branche *dev_nom* et la sélectionner
  * Aller dans le dossier **.gitignore/workflows** et copier le contenu d'un des fichiers présents
  * Créer un nouveau fichier *GithubSync_NOM.yml* et coller le contenu
  * Remplacer par ton nom dans *Sync bot on CSML Studio* et les *CSML_CLIENT_API* et le nom de ta branche (ligne 6)
  * Commit

  ### CSML
  
  * Créer un bot sur https://studio.csml.dev/auth/login
  * Dans **Channel**, ajouter une nouvelle API *GitHubSync* et cliquer sur l'**API** ainsi créée (en haut) pour afficher la page API Keys
  * Retourner sur GitHub, dans le menu **Settings->Secrets** https://github.com/primairepopulaire/PrimPopBot/settings/secrets/actions
  * ajouter 2 variables (new repository secrets):
    * CSML_CLIENT_API_KEY_NOM <-> Copier l'API Key du bot créé dans CSML
    * CSML_CLIENT_API_SECRET_NOM <-> Copier l'API Secret du bot créé dans CSML
  * Dans **<>Code** cliquer sur "Compare & pull request", valider
  * Dans **Actions** une nouvelle action *GithubSync_NOM.yml* est disponible

  ### Comment ça marche ?
  
  * Après une modification du code du bot de votre branche, le code push sur votre branche *dev* se synchronise directement avec votre bot personnel.
  * À cette étape dans le menu Actions, une fois que c'est vert, c'est que la synchro est faite avec le bot
  * **Attention** Un merge de pull request d'une branche *dev* sur la *main* synchronise le bot actuellement utilisé dans le QG ! 

## Règles

	* Une pull request doit toujours être validée par au moins une autre personne.
