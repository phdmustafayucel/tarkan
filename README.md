# Tarkan

Projet versionné avec Git et synchronisé avec GitHub via SSH.
Ce dépôt sert de base propre pour le développement, le versionnement et le travail reproductible.

---

## Prérequis

- macOS / Linux
- Git (version récente)
- Compte GitHub
- Clé SSH configurée et ajoutée à GitHub

---

## Vérification SSH

Vérifier la présence d’une clé SSH :

ls ~/.ssh

Les fichiers attendus :

- id_ed25519
- id_ed25519.pub

Tester la connexion GitHub :

ssh -T git@github.com

Réponse attendue :

You've successfully authenticated, but GitHub does not provide shell access.

---

## Cloner le dépôt

git clone git@github.com:phdmustafayucel/tarkan.git
cd tarkan

IMPORTANT
Après un git clone, il faut toujours entrer dans le dossier cloné avant d’utiliser Git.

---

## Structure du dépôt

tarkan/
├── .git/
├── README.md
└── ...

---

## Commandes Git essentielles

git status

git add .

git commit -m "Message de commit clair"

git push

---

## Erreurs courantes

not a git repository

Cause :
Commande exécutée hors du dossier contenant .git

Solution :

cd tarkan

---

Commandes invalides :

git add*
git add.

Commande correcte :

git add .

---

## Bonnes pratiques

pwd
ls -a

Un commit = une modification logique
Messages de commit courts et explicites

---

## Auteur

PhD Student, Mustafa Yücel
MSc, Berkin Binbas

---

## Licence

À définir.
