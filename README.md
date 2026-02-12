# EPITECH C++ Coding Style Checker - YUM/DNF Repository

This repository hosts RPM packages for the EPITECH C++ Coding Style Checker.

## Installation

### Fedora/RHEL/CentOS

1. Add the repository:

```bash
sudo tee /etc/yum.repos.d/cpp-checker.repo << 'REPO_EOF'
[cpp-checker]
name=EPITECH C++ Coding Style Checker
baseurl=https://philibertg.github.io/cpp-checker-rpm-repo
enabled=1
gpgcheck=0
REPO_EOF
```

2. Install the package:

```bash
sudo dnf install cpp-coding-style-checker
```

3. Update the package:

```bash
sudo dnf upgrade cpp-coding-style-checker
```

## Requirements

- Docker or Podman
- Fedora 38+, RHEL 8+, CentOS 8+, AlmaLinux 8+, Rocky Linux 8+

## Usage

After installation, run:

```bash
cpp-coding-style-checker /path/to/project
cpp-coding-style-checker .  # Check current directory
```

---

# Règles Implémentées V1.0.15

## Fonctions (F)

- **F1** [MAJOR/INFO] : Nombre de lignes (recommandé 20, max 25)
- **F2** [MINOR] : Nombre de colonnes dans les fonctions (max 80)
- **F3** [MAJOR] : Nombre d'arguments (max 5)
- **F4** [MINOR] : Pas de void pour les fonctions sans arguments
- **F5** [MINOR] : Pas de commentaires dans les fonctions
- **F6** [MINOR] : Polymorphisme (virtual/override/final)
- **F7** [MINOR] : Paramètres callables (std::function)
- **F8** [MINOR] : Copy elision (passage par référence)

## Nommage (N)

- **N3** [MINOR] : Noms de fonctions en camelCase
- **N4** [MINOR] : Noms de variables en camelCase

## Classes (K)

- **K2** [MINOR] : Listes d'initialisation des constructeurs
- **K3** [MINOR] : Ordre des modificateurs d'accès

## En-têtes (H)

- **H1** [MAJOR] : Contenu des fichiers d'en-tête
- **H2** [MAJOR] : Gardes d'inclusion (#pragma once interdit)
- **H3** [MINOR] : Macros (préférer const/constexpr)

## Mise en Forme - Layout (L)

- **L1** [MINOR] : Une ligne = un statement
- **L2** [MINOR] : Indentation (4 espaces, pas de tabulations)
- **L3** [MINOR] : Espaces (virgules, keywords, opérateurs)
- **L4** [MINOR] : Placement des accolades
- **L5** [MINOR] : Déclaration de variables
- **L6** [INFO] : Sauts de ligne pour la lisibilité

## Structures de Contrôle (C)

- **C1** [MAJOR] : Branchements conditionnels (max 3 branches, nesting max 2)
- **C2** [MINOR] : Expressions ternaires simples
- **C3** [MAJOR] : Pas de goto
- **C4** [MINOR] : Boucles for simples
- **C5** [INFO] : Préférer les range-based for

## Portée Globale (G)

- **G1** [MINOR] : En-tête de fichier EPITECH

## Avancé (A)

- **A9** [MAJOR] : Pas de using namespace global

---

**Total : 28 règles implémentées**

## Légende

- **MAJOR** : Erreur grave
- **MINOR** : Problème de style
- **INFO** : Avertissement

