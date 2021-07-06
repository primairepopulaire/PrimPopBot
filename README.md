# PrimPopBot

Un chatbot pour https://primairepopulaire.fr/ 

Voir le bot : https://chat.csml.dev/channels/difm7vtdxz0rr16wigcqnk8sbmqkioxi

## Synchronisation GitHub -> CSML

  ### GitHub
  
  * Créer une nouvelle branche *dev_nom* et la sélectionner
  * Aller dans le dossier **.gitignore/workflows** et copier le contenu d'un des fichiers
  * Créer un nouveau fichier *GithubSync_NOM.yml* et coller
  * Remplace par ton nom dans *Sync bot on CSML Studio* et les *CSML_CLIENT_API* et le nom de ta branche (ligne 6)
  * Commit

  ### CSML
  
  * Créer un bot
  * Dans **Channel**, ajouter une nouvelle API *GitHubSync* et aller dans **API** (en haut)
  * Retourner sur GitHub, dans **Settings->Secrets** ajouter 2 variables :
    * CSML_CLIENT_API_KEY_NOM <-> API Key du bot créé
    * CSML_CLIENT_API_SECRET_NOM <-> API Secret
  * Dans **<>Code** cliquer sur "Compare & pull request", valider
  * Dans **Actions** une nouvelle action *GithubSync_NOM.yml* est disponible

  ### Comment ça marche ?
  
  * Le code push sur une branche *dev* se synchronise directement avec le bot. 
  * **Attention** Un merge de pull request d'une branche *dev* sur la *main* synchronise le bot actuellement utilisé dans le QG ! 

## Règles

	* Une pull request doit toujours être validée par au moins une autre personne.
