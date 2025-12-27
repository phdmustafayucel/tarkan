# Tarkan

Version-controlled project using Git and synchronized with GitHub via SSH.
This repository serves as a clean base for development, versioning, and reproducible work.

---

## Prerequisites

- macOS / Linux
- Git (recent version)
- GitHub account
- SSH key configured and added to GitHub

---

## SSH Verification

Check for an existing SSH key:

ls ~/.ssh

Expected files:

- id_ed25519
- id_ed25519.pub

Test the GitHub connection:

ssh -T git@github.com

Expected response:

You've successfully authenticated, but GitHub does not provide shell access.

---

## Clone the Repository

git clone git@github.com:phdmustafayucel/tarkan.git
cd tarkan

IMPORTANT  
After a git clone, you must always enter the cloned directory before using Git.

---

## Repository Structure

tarkan/
├── .git/
├── README.md
└── ...

---

## Essential Git Commands

git status  
git add .  
git commit -m "Clear commit message"  
git push  

---

## Common Errors

not a git repository

Cause:  
Command executed outside the directory containing .git

Solution:

cd tarkan

---

## Invalid Commands

git add*  
git add.

Correct command:

git add .

---

## Best Practices

pwd  
ls -a  

- One commit = one logical change
- Commit messages should be short and explicit

---

## Authors

PhD Student, Mustafa Yücel  
MSc, Berkin Binbas  

---

## License

To be defined.
