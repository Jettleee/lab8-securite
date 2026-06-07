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

<img width="188" height="63" alt="image" src="https://github.com/user-attachments/assets/3a0f9dd2-6ca9-4abb-8e86-ed305e0e7b83" />


L'APK est placee dans le dossier de perimetre. Cette organisation separe clairement l'artefact autorise du reste de l'analyse.

### Structure du workspace

<img width="205" height="290" alt="image" src="https://github.com/user-attachments/assets/b4af35f1-5c6e-4898-89b8-569e879b30f1" />


Les dossiers du lab sont separes par etape: scope, BeVigil, Yaazhini, triage et rapport.

### Preparation des fichiers

<img width="663" height="640" alt="image" src="https://github.com/user-attachments/assets/a7444f28-151a-409c-9e54-ec16f3cdc6ae" />


La structure et les fichiers de tracabilite sont prepares afin de garder une analyse reproductible.

### Informations d'analyse

<img width="679" height="123" alt="image" src="https://github.com/user-attachments/assets/50a7404a-0ce7-4330-ae51-af9ea4f063a0" />


Le fichier d'information regroupe la date, l'analyste, la cible, le hash et l'environnement.

### Hash de l'APK

<img width="598" height="20" alt="image" src="https://github.com/user-attachments/assets/35821792-6c48-40af-b0ae-41f9f9727ced" />


Le hash SHA-256 de l'APK est calcule et documente. Il sert d'identifiant unique pour l'artefact analyse.

### Resultat BeVigil

<img width="913" height="445" alt="image" src="https://github.com/user-attachments/assets/3e38b455-6dd6-4ce9-88ac-ac514d43f21c" />

BeVigil donne une vue synthetique des signaux de securite associes a l'application.

### Analyse Yaazhini

<img width="860" height="329" alt="image" src="https://github.com/user-attachments/assets/743fee80-0269-4e3d-ba03-6c1afa794082" />


Yaazhini presente les resultats dans un tableau qui facilite la lecture des constats.

### Synthese Yaazhini

<img width="798" height="249" alt="image" src="https://github.com/user-attachments/assets/f12148ea-3dc7-4833-91c4-7699dd418c1e" />


La synthese Yaazhini resume les categories detectees et sert de base au triage.

## Resultat

Le lab produit un workspace structure, un artefact identifie par hash, des resultats BeVigil et Yaazhini, puis une base de triage exploitable pour relier les constats aux references OWASP.

## Auteur

Youssef CHARAF
