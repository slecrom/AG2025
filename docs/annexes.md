# 5. Annexes

Cette page regroupe différentes solutions utilisées dans Galaxy au cours des travaux pratiques 

<!---

--------------------------------------------------------------------------------
## Commandes du programme screen

Screen est un programme linux utile qui crée, attache, détache ou rattache des sessions shell "virtuelles". Screen permet d'exécuter des processus linux simultanés dans des environnements isolés qui peuvent être mis en arrière-plan tout en travaillant avec la console à d'autres tâches.

Commandes utiles :

- `screen -ls` liste toutes les sessions screen disponibles, attachées (actuellement actives) ou détachées en arrière-plan ;
- `screen -r <session>` rattache une session écran détachée ;
- `CtrlA puis D` détache la session active ;
- Tapez `exit` pour mettre fin à la session active ;
- `screen -S <session>` crée une nouvelle session.


--------------------------------------------------------------------------------
## Gestion du serveur Galaxy

- `galaxyctl status` donne l'état du serveur galaxy ;
- `galaxyctl start` si d'aventure le serveur galaxy est arrêté, mais cela ne devrait pas arriver ;
- `galaxyctl stop` pour arrêter le serveur, mais il n'y a en principe pas de raison de le faire ;
- `galaxyctl restart` pour redémarrer le serveur, utile si besoin de mettre à jour des références, des changements de préférence, etc. 

Au redémarrage d'une machine virtuelle (VM) suspendue, on retrouve Galaxy dans l'état où il était lors de sa suspension. À noter cependant que si on suspend la VM au milieu d'un job Galaxy en exécution cela mettra le job en question en erreur.

-->


--------------------------------------------------------------------------------
## Résoudre les jobs bloqués dans Galaxy

Si après une réactivation de votre VM dans Galaxy vos jobs sont grisés, le gestionnaire slurm installé sur votre serveur est bloqué.

Pour le relancer, [suivez les indications du tutoriel STARTbio](https://artbio.github.io/startbio/AnalyseGenomes_2025/manage_VM/#3-stalled-jobs-in-your-galaxy-histories).


--------------------------------------------------------------------------------
## Modifier le type des données

Il peut arriver qu'un fichier, pourtant présent dans votre historique, ne soit pas visible en entrée d'un outil Galaxy. Par exemple il peut arriver que le fichier fastq que vous avez chargé dans votre historique n’apparait pas comme disponible dans l’outil Bowtie.

Pour régler ce problème, vous devez réaliser une conversion du type de fichier. L’outil attend un fichier au format fastqsanger et il est pour le moment seulement fastq.gz. 

Pour changer le type d’un fichier, il faut cliquer sur l’icône en forme de crayon. Puis aller dans l’onglet « Datatype ».

![Changer le type des données](img/annexes/change_datatype1.png "Changer le type des données")

Dans le menu déroulant remplacer « fastq.gz », le type actuel, par « fastqsanger.gz ». Puis cliquer sur "Changer le format des données"

![Changer le type des données](img/annexes/change_datatype2.png "Changer le type des données")


--------------------------------------------------------------------------------
## Résoudre les problèmes d'affichage HTML dans Galaxy

Il est possible que les sorties de certains outils ne s'affichent pas dans Galaxy comme par exemple FastQC.

Pour les afficher il faut les autoriser spécifiquement :

1. Aller dans le menu "Admin"
2. Dans le menu de gauche, dans la partie "Tool Management", choisir "Manage Allowlist"
3. Rechercher "FastQC" dans la liste, cliquer sur n'importe quelle case de la ligne. Elle va disparaître et s'afficher dans l'onglet "HTML Rendered"

![Whitelist](img/annexes/whitelist.png "Autoriser l'affichage HTML")

Ce système protège l'injection de code dans les pages HTML.


--------------------------------------------------------------------------------
## Copier des fichiers entre histoires

Pour utiliser dans votre histoire actuel un fichier situé dans un autre histoire il faut procéder de la façon suivante :

1. Choisir "Copier les jeux de données" depuis le menu "roue crantée" en haut à droite
2. Sélectionner les fichiers qui vous intéressent depuis l'histoire source vers l'histoire de destination, vous pouvez aussi indiquer le nom d'une nouvelle histoire
3. Cliquez sur "Copy History Items"

![Copie entre histoires](img/annexes/history_copie.png "Copie de données entre histoires")


--------------------------------------------------------------------------------
## Extraire des éléments d'une collection

Pour extraire des éléments d'une collection, utilisez l'outil ***Extract dataset*** en sélectionnant les fichiers à extraire les un après les autre grâce à leur numéro d'index dans la collection.
	
![Extraire un élément d'une collection](img/annexes/extract_dataset.png "Extraire un élément d'une collection")


--------------------------------------------------------------------------------
## Partage de fichiers dans Galaxy

### Isoler les données à partager dans une histoire dédidée

La première étape consiste à copier les données à partager dans une nouvelle histoire.

![Nouvelle histoire](img/annexes/history_new.png "Nouvelle histoire")

Sélectionnez cette nouvelle histoire, supprimez la collection, affichez les éléments invisibles et rendez-les visibles

![Suppression d'une collection](img/annexes/history_collection_delete.png "Suppression d'une collection")
![Affichage des éléments invisibles](img/annexes/history_unhidde.png "Affichage des éléments invisibles")

Renommez vos éléments pour les rendre plus facile à trouver.

### Partager votre histoire

Pour partager votre histoire, il faut tout d'abord sélectionner « Partager et Publier » dans le menu d'option tout en haut à droite puis choisir « Make History Accessible ».

![Partage d'historique](img/annexes/history_share1.png "Partage d'historique")
![Partage d'historique](img/annexes/history_share2.png "Partage d'historique")

Retournez de nouveau dans le menu en haut à droite, cliquez sur « Exporter l’historique dans un fichier » puis sur le lien "Click here to generate a new archive for this history".

![Export d'historique](img/annexes/history_export.png "Export d'historique")

**Conserver ce lien car c'est lui qui vous permet de partager votre histoire avec d'autres serveurs Galaxy.** Vous pouvez aussi cliquer sur le lien pour récupérer l'historique en local. Attention les données génomiques peuvent être volumineuses !

![URL de l'historique](img/annexes/history_url.png "URL de l'historique")

### Importer une histoire partagée

Pour importer une histoire partagé, allez dans le menu "Utilisateur" puis choisir "Histories". Cliquez sur "Import history" en haut à droite.

![Import d'histoire](img/annexes/history_import.png "Import d'histoire")

Sélectionnez "Export URL from another Galaxy instance" puis collez l'URL de l'histoire que vous voulez récupérer dans le champ "Archived History URL".

![Import d'histoire](img/annexes/history_upload1.png "Import d'histoire")
![Import d'histoire](img/annexes/history_upload2.png "Import d'histoire")

Une fois importé, pensez à le renommer pour lui donner un nom plus explicite.

--------------------------------------------------------------------------------
## Sauvegarde d'une machine virtuelle

### Création d'un instantané

Vous pouvez créer un instantané pour sauvegarder votre disque à des étapes importantes en cas de problème. Par exemple une fois toutes les tutoriels terminés avant de démarrer votre analyse personnelle ou pour augmenter l'espace disponible.

- Allez dans l'application "Instances de VM", cliquer sur le nom de la VM
- Dans la section "Stockage" cliquez sur le nom du disque de démarrage
- Puis cliquez sur "Créer un instantané" dans la barre de menu du haut
- Pramètres
	- Nom : tp-galaxy-ag2025
	- Description : Sauvegarde de la VM du TP AG2025 après les 2 jours de tutoriels
	- Type de source de l'instantané : Disque
	- Disque source : test-galaxy-4
	- Type : instantané
	- Emplacement : Régional - europe-north1

!!! danger "Attention"

	Choisissez l'emplacement là où vous avez créé votre VM.


![Création d'un instantané](img/annexes/snapshot_creation.png "Création d'un instantané")

Vous pouvez obtenir plus d'information en consultant la documentation [Créer des instantanés de disque](https://cloud.google.com/compute/docs/disks/create-snapshots?hl=fr)

### Utilisation d'un instantané

En cas de problème avec votre VM vous pouvez repartir d'une sauvegarde sans être obligé de tout réinstaller.

- La première étape consiste à créer une VM comme vous l'avez déjà fait en suivant [le tutoriel StartBio](https://artbio.github.io/startbio/AnalyseGenomes_2025/Deploy_server_from_VMI/#2-spin-off-your-galaxy-server-from-a-virtual-machine-image).
- Puis dans disque de démarrage cliquer sur "Modifier" et dans l'onglet "Instantanés" choisir celui que vous avez créé.
- Vous avez la possibilité d'augmenter la taille du disque si vous souhaitez obtenir plus d'espace sur votre VM.

![Utilisation d'un instantané](img/annexes/snapshot_utilisation.png "Utilisation d'un instantané")

