# 🧪 Simulation Interactive Atomes & Molécules — 10 CO

> Application pédagogique 3D interactive développée dans le cadre du cours **103.220 – Didactique des sciences, sec I** à la **Haute École Pédagogique du Valais (HEP-VS)**.

---

## 🎯 Objectif pédagogique

Cette simulation permet aux élèves de **10e CO** (niveau secondaire I, Valais, Suisse) d'explorer de manière interactive les concepts fondamentaux de la chimie :

- La **différence entre un atome et une molécule**
- La **structure des molécules** en 3D (géométrie VSEPR, liaisons covalentes)
- La **construction de molécules** par assemblage d'atomes
- La **validation chimique** des structures créées (liaisons respectées, règle de l'octet)
- Le **mode comparaison** pour visualiser deux molécules côte à côte

L'application s'inscrit dans une démarche de **transposition didactique** : rendre accessibles des concepts scientifiques complexes (modèle quantique, hybridation) à travers des représentations simplifiées et interactives, tout en respectant la rigueur scientifique.

---

## ✨ Fonctionnalités principales

| Fonctionnalité | Description |
|---|---|
| 🔬 Galerie de molécules | Plus de 40 molécules prédéfinies (H₂O, CO₂, CH₄, fullerène C₆₀, acides aminés…) |
| 🏗️ Construction libre | Ajouter/supprimer des atomes et former des liaisons |
| ✅ Validation chimique | Feedback coloré : vert (molécule connue), orange (hypothétique valide), rouge (invalide) |
| 🔄 Comparaison | Afficher deux molécules simultanément avec contrôle de la distance |
| 📷 Mode caméra AR | Fond de caméra réelle pour un effet de réalité augmentée |
| 🎓 Mode pédagogique | Interface simplifiée avec guide intégré (modèle de Bohr, nuage électronique) |
| 🌐 Simulation physique | Répulsion de Coulomb + contraintes de liaisons pour des formes réalistes |
| 🏆 Quiz / Jeu | Mode jeu avec confettis pour récompenser la réussite |

---

## 🖥️ Technologies utilisées

| Technologie | Version | Rôle |
|---|---|---|
| [React](https://react.dev/) | 18.x | Interface utilisateur |
| [Three.js](https://threejs.org/) | 0.160.x | Rendu 3D |
| [@react-three/fiber](https://docs.pmnd.rs/react-three-fiber) | 8.x | Intégration React + Three.js |
| [@react-three/drei](https://github.com/pmndrs/drei) | 9.x | Composants 3D utilitaires |
| [Vite](https://vitejs.dev/) | 5.x | Bundler (build unique fichier HTML) |
| [canvas-confetti](https://github.com/catdad/canvas-confetti) | 1.9.x | Animations de célébration |

---

## 📁 Structure du projet

```
transposition didactique/
│
├── 📄 index_pedagogique_v13.1.html   ← Application principale (build autonome)
├── 📄 README.md                       ← Ce fichier
├── 📄 LANCER.bat                      ← Script de lancement rapide (Windows)
│
└── 📁 interactive-molecule-app/       ← Code source
    ├── 📁 src/
    │   ├── App.jsx                    ← Application principale
    │   ├── App_Pedagogique.jsx        ← Version pédagogique guidée
    │   ├── molecules_data.js          ← Base de données des molécules
    │   ├── MolecularCloud.jsx         ← Nuages électroniques / orbitales
    │   ├── HEPVSLogo.jsx              ← Logo HEP-VS intégré
    │   └── RetroUFO.jsx               ← Animation ludique
    ├── package.json
    ├── vite.config.js
    └── vite.config.pedagogique.js
```

---

## 🚀 Utilisation (sans installation)

Le fichier **`index_pedagogique_v13.1.html`** est **entièrement autonome** (toutes les bibliothèques sont intégrées). Il suffit de :

1. Télécharger le fichier `index_pedagogique_v13.1.html`
2. L'ouvrir dans un navigateur moderne (Chrome, Firefox, Edge)
3. **Aucune connexion internet requise**

> ⚠️ Pour le mode caméra (AR), autoriser l'accès à la webcam dans le navigateur.

---

## 🛠️ Développement (pour contributions)

### Prérequis
- [Node.js](https://nodejs.org/) ≥ 18
- npm ≥ 9

### Installation

```bash
cd interactive-molecule-app
npm install
```

### Lancement en mode développement

```bash
npm run dev          # Application standard
npm run dev:ped      # Mode pédagogique
```

### Build (génère un fichier HTML autonome)

```bash
npm run build        # → dist/index.html
npm run build:ped    # → dist/index_pedagogique.html
```

---

## 📚 Contexte académique

Ce projet a été développé dans le cadre du module **103.220 – Didactique des sciences (secondaire I)** à la HEP-VS.

Il illustre le concept de **transposition didactique** (Chevallard, 1985) : adapter le **savoir savant** (chimie quantique, hybridation des orbitales) en un **savoir enseignable** accessible aux élèves de 10e CO, en passant par différents niveaux de modélisation (modèle de Bohr simplifié → modèle 3D interactif → nuages électroniques).

### Objectifs du MER (Moyen d'Enseignement Romand) couverts

- Distinguer atome et molécule
- Représenter et nommer des molécules simples (H₂O, O₂, N₂, CO₂, CH₄, NH₃…)
- Comprendre la notion de liaison chimique
- Relier structure moléculaire et propriétés (forme, polarité)

---

## 👨‍🏫 Auteur

Développé par un enseignant en formation à la **HEP-VS** (Haute École Pédagogique du Valais), avec l'assistance de l'IA **Antigravity (Google DeepMind)**.

---

## 📄 Licence

Ce projet est destiné à un usage **éducatif et non commercial**.  
Les bibliothèques tierces (React, Three.js, etc.) sont soumises à leurs licences respectives (MIT).

---

*Dernière mise à jour : mars 2026 — Version 13.1*
