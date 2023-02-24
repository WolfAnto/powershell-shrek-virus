# powershell-shrek-virus

# Fonctionnalités
- Modification du fond d'écran
- Ajout d'icônes Shrek sur le Bureau Windows
- Nom aléatoire des icônes Shrek
- Augmentation du volume de l'ordinateur
- Voix TTS


# Démonstration
[![Watch the video](https://i.imgur.com/vKb2F1B.png)](https://user-images.githubusercontent.com/73076854/213131127-e1d940fc-7631-4291-b21a-8ce56d1593c2.mp4)


# Prérequie
- Pour le bon fonctionnement du script Powershell, le nom du fichier ne doit pas être modifier !
- Windows à jours
- L'environnement Bureau de la victime ne doit pas etre sur OneDrive

# Installation
- Télécharger ce dépôt
```
git clone https://github.com/WolfAnto/powershell-shrek-virus/
Sinon via interface graphique
```
- Execution du script
```
Clique droit sur ShrekMenu.ps1 > Exécuter en Powershell
```


# Explication / Fonctionnement

Le script est un menu Powershell qui vous propose diverse options :
- Installation Silencieuse
- Mode Flagrant
- Seulement le fond d'écran
- Seulement les icônes
- Seulement la voix TTS
- Seulement la notification Windows
- Désinstallation du script sur la machine
- Quitter le script

### Installation Silencieuse
- Lors de l'éxécution de cette option, le script va télécharger un script Powershell et venir l'installer dans le répertoire "C:\Users\Public\Documents"
- Ensuite le script va télécharger un script CMD et l'installer dans "C:\Users\username\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup\VirtualBox.cmd"
- Cela va permettre d'installer le script Powershell sur la machine mais aussi l'éxecuter lors du démarrage de l'ordinateur.


### Mode Flagrant
- Lors de l'éxécution de cette option, le script va s'éxécuter instentanément et il va définir un nouveau fond d'écran, créer un nombre prédéfinis d'icones sur le bureau avec un nom aléatoire, et faire une installation silencieuse.

### Seulement le fond d'écran
- Lors de l'éxécution de cette option, le script va uniquement changer le fond d'écran de l'ordinateur.

### Seulement les icônes
- Lors de l'éxécution de cette option, le script va vous demandez combien d'icônes souhaitez vous créer sur le Bureau Windows.

###  Seulement la voix TTS
- Lors de l'éxécution de cette option, le script va augmenter le volume de l'ordinateur au maximum et utiliser la fonction Text To Speach pour citez une phrase.

### Seulement la notification Windows
- Lors de l'éxécution de cette option, le script va utiliser une fonction Windows pour faire apparaitre une notification en bas de l'écran avec une phrase prédéfini.

### Désinstallation du script sur la machine
- Lors de l'éxécution de cette option, le script va supprimer les traces du script, changer le fond d'écran, supprimer les icônes du Bureau Windows, et ne plus s'éxecuter lors du démarrage

### Quitter
- Lors de l'éxécution de cette option, le script va se fermer.

# Modification
Si vous souhaitez changer le fond d'écran, dans le script Powershell ShrekMenu.ps1 :
- Convertir votre image servant de fond d'écran en code base64
- Aller à la ligne 72 et remplacer le code base64 par le votre

Si vous souhaitez changer l'icône, dans le script Powershell ShrekMenu.ps1 :
- Convertir votre image servant de fond d'écran en code base64
- Aller à la ligne 84 et remplacer le code base64 par le votre

