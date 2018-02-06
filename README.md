# Chocolatey

Fichiers d'installation des logiciels à l'aide de chocolatey.

# Installation de chocolatey sur un poste

- Utiliser le fichier `installation_chocolatey.ps1`

# Installation des logiciels de base sur un poste

- En local 

```
iex ((new-object net.webClient).DownloadString('https://raw.githubusercontent.com/DLatreyte/chocolatey/master/logiciels_base.ps1'))
```

- À distance (en utilisant PowerShell)

