# StarTrace — distribution

Ce dépôt ne contient **aucun code source**. Il sert uniquement à distribuer
les versions de StarTrace et à publier le numéro de la plus récente.

StarTrace est un utilitaire Windows de diagnostic pour Star Citizen :
il examine les traces laissées par le jeu, en explique prudemment le contenu,
et prépare un dossier d'assistance anonymisé. Il ne modifie jamais
l'installation du jeu.

## Télécharger

Les installeurs se trouvent dans [Releases](../../releases).

Prenez `.msi` ou `.exe`, puis lancez-le. Windows peut avertir que l'éditeur
est inconnu : ces installeurs ne sont pas signés.

## Vérifier un téléchargement

Chaque release contient un fichier `SHA256SUMS.txt`. Comparez l'empreinte du
fichier téléchargé avec celle qui y figure :

```powershell
Get-FileHash .\StarTrace_1.0.0_x64-setup.exe -Algorithm SHA256
```

## `latest.json`

Le fichier [`latest.json`](latest.json) annonce la dernière version publiée.
StarTrace le lit quand vous le lui demandez, pour vous signaler qu'une version
plus récente existe.

Il ne contient que deux champs, et aucune donnée sur qui le consulte :

```json
{ "version": "1.0.0", "releaseUrl": "https://..." }
```

L'application ne télécharge ni n'installe jamais rien d'elle-même : elle
propose seulement d'ouvrir la page de la release dans votre navigateur.
