# LabSec8 - Analyse statique Android

## Auteur

Youssef CHARAF

## Objectif

Ce lab presente une analyse statique encadree de l'APK pedagogique OWASP MSTG UnCrackable Level 1. Le travail couvre le perimetre, la tracabilite, l'identification de l'artefact, l'analyse avec BeVigil et Yaazhini, puis le triage des constats.

## Cible

- APK: `UnCrackable-Level1.apk`
- Hash SHA-256: `1DA8BF57D266109F9A07C01BF7111A1975CE01F190B9D914BCD3AE3DBEF96F21`
- Provenance: support de cours
- Environnement: Windows 11 Pro

## Demarche

Le dossier `00-scope` contient le perimetre de l'analyse. Il precise que la cible est un APK pedagogique autorise et que le travail reste limite au cadre du lab.

Le workspace est organise en dossiers separes: `00-scope`, `01-bevigil`, `02-yaazhini`, `03-triage` et `04-report`. Les fichiers `analyse_info.txt` et `commands.log` gardent la trace de l'environnement, de l'artefact et des commandes importantes.

L'APK est copiee dans le dossier de scope, puis son hash SHA-256 est calcule. Ce hash identifie l'artefact analyse et permet de verifier que les resultats correspondent au bon fichier.

BeVigil est utilise pour obtenir une premiere vue des informations exposees autour de l'application. Les resultats sont conserves comme pistes d'analyse.

Yaazhini est utilise pour analyser le contenu de l'APK. Les resultats sont consultes pour relever les categories de risque et preparer le triage.

Les constats sont consolides dans le triage afin d'eviter les doublons entre les outils. Les elements importants sont ensuite relies aux categories OWASP MASVS lorsque la correspondance est pertinente.

## Auteur

Youssef CHARAF

## Preuves

### Dossier de scope

![Dossier scope](<screens/Capture d'écran 2026-06-01 093752.png>)

L'APK est placee dans le dossier de perimetre. Cette organisation separe clairement l'artefact autorise du reste de l'analyse.

### Structure du workspace

![Structure du workspace](<screens/Capture d'écran 2026-06-01 093533.png>)

Les dossiers du lab sont separes par etape: scope, BeVigil, Yaazhini, triage et rapport.

### Preparation des fichiers

![Preparation](<screens/Capture d'écran 2026-06-01 093606.png>)

La structure et les fichiers de tracabilite sont prepares afin de garder une analyse reproductible.

### Informations d'analyse

![Informations analyse](<screens/Capture d'écran 2026-06-01 093711.png>)

Le fichier d'information regroupe la date, l'analyste, la cible, le hash et l'environnement.

### Hash de l'APK

![Hash APK](<screens/Capture d'écran 2026-06-01 093738.png>)

Le hash SHA-256 de l'APK est calcule et documente. Il sert d'identifiant unique pour l'artefact analyse.

### Resultat BeVigil

![BeVigil](<screens/Capture d'écran 2026-06-01 095300.png>)

BeVigil donne une vue synthetique des signaux de securite associes a l'application.

### Analyse Yaazhini

![Yaazhini tableau](<screens/Capture d'écran 2026-06-01 095324.png>)

Yaazhini presente les resultats dans un tableau qui facilite la lecture des constats.

### Synthese Yaazhini

![Yaazhini synthese](<screens/Capture d'écran 2026-06-01 095334.png>)

La synthese Yaazhini resume les categories detectees et sert de base au triage.

## Resultat

Le lab produit un workspace structure, un artefact identifie par hash, des resultats BeVigil et Yaazhini, puis une base de triage exploitable pour relier les constats aux references OWASP.

## Auteur

Youssef CHARAF
