# Installer Dolibarr

Dolibarr est un ERP open source permettant toute la gestion de votre infrastructure. Grâce à l'association entre WPshop et Dolibarr, nous assurons la conformité aux normes RGPD françaises.

## Téléchargement de Dolibarr

* [Télécharger Dolibarr](https://www.dolibarr.fr/telechargements)
* [Installer Dolibarr](https://wiki.dolibarr.org/index.php/Installation_-_Mise_%C3%A0_jour)

## Synchronisation WPshop & Dolibarr

Pour pouvoir associer les deux, nous allons devoir installer et configurer un module qui va servir de passerelle.

### Génération de la clé secrète WordPress

* Rendez-vous sur votre profil utilisateur dans l'administration de votre WordPress (https://<votrewordpress.ext/profile.php)
* Dans la section WPshopAPI, nous retrouvons le champ API Key. Cliquer sur l'icone: ![](https://github.com/Eoxia/wpshop-docs/blob/master/images/generate-api-key.PNG)
* Sauvegardez la clé apparaissant dans le champs

### Génération de la clé secrète Dolibarr

* Rendez vous dans l'administration de Dolibarr
* Dans accueil/configuration/"modules/applications"
* Activer le module "API/Web services (serveur REST)"
* Cliquez sur le lien de votre profil par exemple : "Super Admin" en haut à droite de l'application, puis sur "fiche".
* Cherchez le champ "Clé pour l'API" puis cliquer sur l'icone: ![](https://github.com/Eoxia/wpshop-docs/blob/master/images/generate-api-key-doli.PNG)
* Si le champs "Clé pour l'API" n'est pas en présent, en dessous de "Mot de passe" vérifier l'activation de l'API REST
* Cliquez sur modifier puis généré la clés pour l'API : par exemple "99FV3H92hgiXu0IyAMEHF8j8Dr89xkca"
* Sauvegardez la clé apparaissant dans le champs

### Installation du module

* Télécharger le ZIP en cliquant [sur github DolibarrWshop](https://github.com/Eoxia/dolibarrwpshop).
* Dézipper et envoyer le dossier wpshop dans le répertoire /custom/ de votre dossier Dolibarr.
* Activer le module dans le menu Modules/Applications en pied de page sur votre Dolibarr.

### Configuration du module

Toujours sur Dolibarr, cliquez sur "Modifier" sur la page de configuration du module :

* WordPress URL: <https://<votredolibarr.ext>
* WordPress secret: La clé récupéré depuis **WordPress**

Du coté de WordPress, rendez-vous dans "WPshop -> Réglages" :

* Dolibarr URL: https://<votrewordpress.ext>
* Dolibarr secret: La clé récupérée depuis **Dolibarr**

### Problèmes connues

#### Connexion WPshop vers Dolibarr ne fonctionne pas (En cours de PR vers Dolibarr)

Le problème vient généralement des serveurs NGINX.
Si vous vous connectez sur la rest API de dolibarr (a finir)
  
  La connexion doit être effectif maintenant, si celà ne marche toujours pas, veuillez ouvrir une issue https://github.com/Eoxia/wpshop-docs/issues

