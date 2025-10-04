# 📦 Gestion Scientifique de Stock (Modèles de Wilson – Notebook + Fichiers Excel)

Projet universitaire réalisé dans le cadre de la **Licence en Recherche Opérationnelle** à l’**USTHB**.  
Ce projet implémente plusieurs **modèles de Wilson (EOQ)** pour l’optimisation scientifique de la gestion des stocks, à travers un **notebook Jupyter** et **quatre fichiers Excel d’entrée** correspondant aux différents cas étudiés.

---

## 🧠 Objectif du projet

L’objectif est de fournir un outil interactif permettant :
- de calculer la **quantité économique de commande (EOQ)** selon plusieurs variantes du **modèle de Wilson** ;
- d’analyser les **coûts totaux moyens** et les contraintes d’approvisionnement ;
- d’expérimenter différents scénarios (avenir certain, incertain, avec contrainte, avec pénurie) ;
- de visualiser les résultats directement depuis un **notebook Jupyter**.

---

## 🧮 Modèles inclus

| Modèle | Fichier Excel associé | Description |
|--------|------------------------|--------------|
| 🔹 Wilson en avenir certain | `WilsonAvenirCertain.xlsx` | Cas simple sans contrainte (demande et délais constants). |
| 🔹 Wilson en avenir certain avec contrainte | `WilsonAvenirCertainAvecContrainte.xlsx` | Intègre une contrainte (capacité, fréquence ou investissement). |
| 🔹 Wilson avec coût de pénurie | `Wilson avec coût de pénurie.xlsx` | Ajoute le coût lié aux ruptures de stock. |
| 🔹 Wilson en avenir incertain | `WilsonAvenirIncertain.xlsx` | Considère la variabilité de la demande (approche stochastique). |

> Chaque fichier Excel contient les paramètres nécessaires au calcul et peut être modifié librement pour tester d’autres cas.

---

## ⚙️ Technologies utilisées

- **Langage :** Python 3  
- **Interface :** Jupyter Notebook  
- **Bibliothèques :**
  - `pandas` → lecture et manipulation de fichiers Excel  
  - `numpy` → calculs mathématiques  
  - `openpyxl` → lecture/écriture Excel  
  - *(optionnel)* `matplotlib` → visualisation graphique  

---

## ▶️ Lancer le projet

### Option 1 — Local (Jupyter)
```bash
# 1. Cloner le dépôt
git clone https://github.com/Tikinas/Projet-de-gestion-de-stock.git
cd Projet-de-gestion-de-stock

# 2. Installer les dépendances
pip install jupyter pandas openpyxl numpy matplotlib

# 3. Lancer le notebook
jupyter notebook
# Puis ouvrir : modele_de_wilson.ipynb
```

### Option 2 — Google Colab
- Ouvre [Google Colab](https://colab.research.google.com)
- Téléverse le notebook `modele_de_wilson.ipynb`
- Téléverse aussi les fichiers Excel (`WilsonAvenirCertain.xlsx`, etc.)
- Ajoute au besoin :
  ```python
  !pip install pandas openpyxl numpy matplotlib
  ```

---

## 📂 Structure du projet

```
.
├── modele_de_wilson.ipynb
├── WilsonAvenirCertain.xlsx
├── WilsonAvenirCertainAvecContrainte.xlsx
├── WilsonAvenirIncertain.xlsx
├── Wilson avec coût de pénurie.xlsx
└── README.md
```

---

## 📊 Exemple d’exécution

```python
import pandas as pd

# Exemple : lecture du cas "Wilson avec coût de pénurie"
data = pd.read_excel("Wilson avec coût de pénurie.xlsx")
print(data)
```

Résultat attendu :
```
   Demande (Co)  Délai (t)  Coût commande (Cr)  Coût possession (Ce)  Coût pénurie (Cp)
0          1000           1                500                   100                300
```

---

## 🧩 Bonnes pratiques

- Garder la **même unité de temps** pour la demande et le délai.  
- Vérifier que les colonnes de vos fichiers Excel correspondent aux variables utilisées dans le notebook.  
- Adapter les en-têtes si nécessaire :  
  par ex. `"Coût de commande"` → `Cr`, `"Coût de possession"` → `Ce`.  

---

## 👥 Équipe du projet

> **Auteurs :**  
> - Tikinas ABBOUD  
> - Merabet Messaoud Warda  
>
> **Encadrant :**  
> Pr. CHAABANE Djamal – Université des Sciences et de la Technologie Houari Boumediene  

---

## 📜 Licence

Projet académique réalisé dans le cadre de la **Licence Recherche Opérationnelle – USTHB**.  
Usage libre pour l’apprentissage et la recherche.
