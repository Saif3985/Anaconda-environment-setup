# Anaconda Environment Setup Guide 🐍

A comprehensive tutorial for creating and managing Python environments using Anaconda, perfect for data science and machine learning projects.

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Anaconda](https://img.shields.io/badge/Anaconda-44A833?style=flat&logo=anaconda&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green.svg)

## 📋 Table of Contents
- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Installation Guide](#installation-guide)
- [Environment Management](#environment-management)
- [Package Installation](#package-installation)
- [VS Code Integration](#vs-code-integration)
- [Troubleshooting](#troubleshooting)

## 🎯 Overview

This guide walks you through the complete process of:
- Installing Anaconda on your system
- Creating isolated Python environments
- Managing dependencies with `requirements.txt`
- Installing packages efficiently
- Integrating with VS Code

Perfect for beginners starting with data science or anyone looking to manage Python environments professionally.

## 🔧 Prerequisites

- Windows, macOS, or Linux operating system
- At least 3GB of free disk space
- Administrator/root access for installation

## 📥 Installation Guide

### Step 1: Download Anaconda

1. Visit the official Anaconda website: [https://www.anaconda.com/](https://www.anaconda.com/)
2. Download the installer for your operating system
3. Run the installer and follow the on-screen instructions

### Step 2: Open Anaconda Prompt

**Windows:**
```bash
Start Menu → Search "Anaconda Prompt" → Open
```

**macOS/Linux:**
```bash
Open Terminal
```

## 🌍 Environment Management

### List All Environments

```bash
conda env list
```

### Create a New Environment

```bash
conda create --name myenv python=3.9
```

Replace:
- `myenv` with your preferred environment name
- `3.9` with your desired Python version

Press `Y` when prompted to proceed.

### Activate the Environment

```bash
conda activate myenv
```

You'll see `(myenv)` appear before your prompt, confirming activation.

### Deactivate the Environment

```bash
conda deactivate
```

### Remove an Environment

```bash
conda remove --name myenv --all
```

## 📦 Package Installation

### Method 1: Install Individual Packages

```bash
# Activate your environment first
conda activate myenv

# Install packages
conda install numpy pandas matplotlib
# or
pip install numpy pandas matplotlib
```

### Method 2: Using requirements.txt (Recommended)

#### Create requirements.txt

Create a file named `requirements.txt` with your dependencies:

```txt
numpy==1.24.3
pandas==2.0.3
matplotlib==3.7.2
seaborn==0.12.2
scikit-learn==1.3.0
jupyter==1.0.0
```

#### Install from requirements.txt

```bash
# Navigate to the directory containing requirements.txt
cd path/to/directory

# Install all packages
pip install -r requirements.txt
```

### Verify Installation

```bash
# Start Python
python

# Try importing
import numpy as np
print(np.__version__)
```

If no errors appear, installation was successful!

## 💻 VS Code Integration

### Open VS Code from Anaconda Prompt

```bash
# Navigate to your project directory
cd path/to/project

# Activate your environment
conda activate myenv

# Open VS Code
code .
```

### Select Python Interpreter in VS Code

1. Open Command Palette: `Ctrl+Shift+P` (Windows/Linux) or `Cmd+Shift+P` (macOS)
2. Type "Python: Select Interpreter"
3. Choose your conda environment (e.g., `myenv`)

## 🛠️ Troubleshooting

### Issue: "conda: command not found"

**Solution:** Anaconda not added to PATH. Reinstall and check "Add to PATH" option.

### Issue: Environment activation fails

**Solution:** 
```bash
# Initialize conda for your shell
conda init

# Restart terminal and try again
conda activate myenv
```

### Issue: Package installation fails

**Solution:**
```bash
# Update conda
conda update conda

# Try installing again
pip install -r requirements.txt
```

### Issue: Wrong Python version in environment

**Solution:**
```bash
# Create new environment with specific version
conda create --name myenv python=3.9 --force
```

## 📚 Common Commands Cheat Sheet

```bash
# List environments
conda env list

# Create environment
conda create --name myenv python=3.9

# Activate environment
conda activate myenv

# Deactivate environment
conda deactivate

# Install package
conda install package_name
pip install package_name

# Install from requirements.txt
pip install -r requirements.txt

# Export environment
conda env export > environment.yml

# Create from environment.yml
conda env create -f environment.yml

# Remove environment
conda remove --name myenv --all

# Update conda
conda update conda

# List installed packages
conda list
pip list
```

## 📁 Sample Project Structure

```
my-project/
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
│   └── analysis.ipynb
├── src/
│   └── main.py
├── requirements.txt
├── README.md
└── environment.yml
```

## 🎓 Best Practices

1. **Use separate environments** for different projects
2. **Document dependencies** in `requirements.txt`
3. **Use version pinning** for reproducibility (e.g., `numpy==1.24.3`)
4. **Keep base environment clean** - don't install packages in base
5. **Regular updates** - `conda update --all` periodically
6. **Export environments** - `conda env export > environment.yml` for sharing

## 🔗 Useful Resources

- [Anaconda Documentation](https://docs.anaconda.com/)
- [Conda Cheat Sheet](https://docs.conda.io/projects/conda/en/latest/user-guide/cheatsheet.html)
- [Managing Environments](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)

## 📧 Questions?

If you encounter issues or have questions, feel free to open an issue on this repository.

## 📄 License

This project is licensed under the MIT License.

---
Made with ❤️ for the Data Science community
