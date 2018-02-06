# Chocolatey

Notes pour l'utilisation de Chocolatey.

# Modification à apporter à PowerShell

```
Set-ExecutionPolicy remotesigned
```

# Installation de chocolatey sur un poste

- Utiliser le fichier `installation_chocolatey.ps1`

# Installation des logiciels de base sur un poste

- En local 

```
iex ((new-object net.webClient).DownloadString('https://raw.githubusercontent.com/DLatreyte/chocolatey/master/logiciels_base.ps1'))
```

- À distance (en utilisant PowerShell)

    - Déclaration des ordinateurs cible

```
$workstations = (“computer1″,”computer2″,”computer3”)
```

    - Installation

```
Invoke-Command -ComputerName $workstations -ScriptBlock {choco install firefox -y | Select-String -Pattern “Chocolatey installed” } | select PSComputername,Line
```

