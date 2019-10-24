# Good coding practices for Data Scientist beginners

This page was originally written to guide my "Python pour le data scientist" students through the coding part of the data science work. 

Coding for ML should not be restricted to opening jupyter notebooks, and for your co-workers/co-researchers's sake, you should make your code as clear and **reproductible** as possible. This requires not only to get to know coding conventions, but also to understand some very basic parts of how a computer works.

This note is not intented to be a complete computer science course, and is only meant to be an agregation of the most useful coding tips I've learned and wished I had been taught. I am not a specialist of coding conventions, or coding efficiency, and if there are some mistakes in that page, feel free to report on the github repo. I just think that, even if data scientists are not developpers, they should have some autonomy with coding, and understand some basics.

The note is thus organized in four themes: 
- *OS/command line*, which will remain very basic (it is meant for data scientists, not developpers!). The most important part for a data scientist is the remote part, as most data scientist will have to execute code on remote servers or virtual instances.
- *Versioning, packaging, reproductibility*, which focus on git, virtual environments, and introduces things like docker.
- *Computational efficiency tips*, which focus on how to parallelize code with python (this will rmain basic), how not to overload RAM, and some mistakes to avoid.
- *Python coding conventions and tips*, which is less useful as it is mainly for your code's aethetics, but can be welcomed when wanting to use automatic tools to, for instance, automatically generate documentation.


# General OS/computer-related skills

## 0. Operating System


## 1. Command line

### 1.1 What is a command line?

### 1.2 Navigating 

### 1.3 Installing programs


## 2. Remote coding

### 2.1 SSH

### 2.2 Screen and equivalents

### 2.3 Sharing files, Synchronizing directories

### 2.4 VSCode remote extension


# Code versioning and packaging, reproductibility

## 1. Versioning

### 1.1 What is code versioning?

### 1.2 Git introduction

### 1.3 Github, gitlab

## 2. Environments

### 2.1 Why using virtual environments? 

### 2.2 Conda, Miniconda

### 2.3 Virtual env, pip

## 3. Other ressources

### 3.1 How to create a pypi package?

### 3.2 Docker

# Computational efficiency tips

### 1. Multiprocessing

### 2. Garbage collector

### 3. Some mistakes I've made that you could avoid

# Python coding conventions and tips

## 1. PEP8

### 1.1 What is PEP8?

### 1.2 Linters

### 1.3 Cheating : Black

## 2. Documenting your code

### 2.1 Docstrings

### 2.2 Automatically generate a documentation

### 2.3 Publish your documentation online



