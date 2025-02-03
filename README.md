# AymeeJaquemyns.github.io
Portfolio

# Mon Portfolio

Ce site est mon portfolio personnel, hébergé via **GitHub Pages**.

## Comment le voir en ligne ?
- Rendez-vous sur **https://AymeeJaquemyns.github.io/**

## Technologies utilisées
- HTML, CSS, JavaScript

## Comment modifier ?
- Clonez ce repo avec :
  ```bash
  git clone https://github.com/AymeeJaquemyns/portfolio.git
  ```
- Modifiez les fichiers et poussez les changements sur GitHub.

.github/workflows/deploy.yml (optionnel) :

name: Déploiement GitHub Pages

on:
  push:
    branches:
      - main

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout du code
        uses: actions/checkout@v2
      - name: Déploiement sur GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./
