# E-Teach

Plans de classe et suivi des élèves en séance, pour Windows. L'application
fonctionne entièrement hors ligne ; les données restent chiffrées sur
l'ordinateur.

Ce dépôt ne contient aucun code : uniquement les installateurs, publiés dans les
[Releases](../../releases).

## Mettre à jour depuis l'application

Après le déverrouillage, E-Teach regarde si une nouvelle version est publiée ici
et l'annonce par un bandeau sur l'accueil. « Installer… » montre ce qui change,
puis télécharge l'installateur, vérifie qu'il vient bien de l'auteur, ferme
E-Teach et lance l'installation. Il suffit de relancer E-Teach à la fin.

Cette recherche n'envoie rien d'autre que la demande elle-même. Elle se
désactive dans Paramètres → À propos → Mises à jour.

## Installer ou mettre à jour à la main

1. Ouvrir la [dernière version](../../releases/latest) et télécharger le fichier
   `E-Teach-X.Y.Z.msi`.
2. L'exécuter. Aucun droit administrateur n'est nécessaire.
3. Windows peut afficher « Windows a protégé votre ordinateur » : l'installateur
   n'est pas signé. Cliquer sur « Informations complémentaires », puis
   « Exécuter quand même ».

Une nouvelle version s'installe par-dessus l'ancienne : inutile de désinstaller.
Les classes, les plans et les séances sont conservés.

Avant une mise à jour, une sauvegarde chiffrée sur clé USB (Paramètres →
Sauvegarde) reste une bonne habitude.

## Vérifier le fichier téléchargé (facultatif)

Chaque version est accompagnée d'un fichier `.sha256`. Les fichiers
`update.txt` et `update.sig` servent à l'application et n'ont pas à être
téléchargés. Dans PowerShell, depuis le
dossier de téléchargement :

```powershell
Get-FileHash .\E-Teach-X.Y.Z.msi -Algorithm SHA256
```

La valeur affichée doit être celle du fichier `.sha256`.

## Désinstaller

Paramètres Windows → Applications → E-Teach → Désinstaller. Les données ne sont
pas supprimées.
