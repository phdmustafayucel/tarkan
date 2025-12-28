# Tarkan

Version-controlled project using Git and synchronized with GitHub via SSH.  
This repository provides a clean and reproducible base for development and research-oriented workflows.

---

## Overview

Tarkan is a lightweight Git-based project template designed to enforce good
version control practices and reproducible development.
It is intended as a solid starting point for technical or academic projects.

---

## Purpose

- Provide a clean Git/GitHub workflow
- Enforce good versioning habits
- Serve as a reproducible development base
- Prevent common Git mistakes

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

## Getting Started

1. Ensure SSH is properly configured
2. Clone the repository
3. Enter the project directory
4. Start working

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
git commit -m "Clear and descriptive commit message"  
git push  

---

## Recommended Workflow

1. Make a single logical change
2. Check repository status
3. Stage changes
4. Commit with a clear message
5. Push to GitHub

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

- One commit equals one logical change
- Commit messages should be short, explicit, and meaningful

---

## Contributing

- Keep commits atomic
- Do not commit generated or temporary files
- Follow the recommended workflow

---

## Authors

PhD Student, Mustafa Yücel  
MSc, Berkin Binbas  

---

## License

This project is currently unlicensed.  
All rights reserved.
