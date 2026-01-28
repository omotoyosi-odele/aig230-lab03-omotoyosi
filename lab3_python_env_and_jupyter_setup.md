
# Lab 3 – Text Representation and Statistical Language Models
Python Environment and Jupyter Setup

Follow **all steps in order**. Do not skip steps.

---

## Part A. Navigate to the Correct Project Folder

Open **Git Bash** and navigate to your Lab 3 folder:

```bash
cd "~/Documents/Seneca Polytechnic/AIG230 - NLP/labs/aig-230-lab03"
```

Confirm location:

```bash
pwd
```

---

## Part B. Create the Virtual Environment

```bash
python -m venv aig230-env
```

---

## Part C. Activate the Environment

```bash
source "aig230-env/Scripts/activate"
```

---

## Part D. Install Required Packages

```bash
pip install --upgrade pip
pip install jupyter ipykernel numpy pandas scikit-learn nltk joblib
```

---

## Part E. Register the Environment as a Jupyter Kernel

```bash
python -m ipykernel install --user   --name aig230-env   --display-name "Python (AIG230)"
```

---

## Required Folder Structure

```
aig-230-lab03/
├─ aig230-env/
├─ Lab3_Text_Representation.ipynb
├─ Lab3_Statistical_Language_Models.ipynb
├─ README.md
├─ requirements.txt
```

---
