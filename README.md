# 📡 Analyse de données réseau mobile  
Analyse d’un jeu de données simulant le comportement d’antennes mobiles, dans un contexte proche des activités de supervision réseau (télécom).

---

## 🎯 Objectif du projet
L’objectif est d’identifier, visualiser et comprendre les anomalies réseau (latence, débit, erreurs radio, température) afin de :
- détecter les antennes problématiques,
- déterminer les heures critiques d’instabilité,
- comparer une antenne instable avec une antenne saine,
- formuler des recommandations pour améliorer la qualité de service.

Ce projet reproduit le travail d’un **Data Analyst Réseau / Ingénieur Supervision** dans un opérateur télécom.

---

## 📊 Analyses réalisées

### 🔎 1. Exploration des données
- Nettoyage et structuration du dataset  
- Analyse des métriques clés :  
  - `latence_ms`  
  - `debit_mbps`  
  - `taux_erreur_%`  
  - `temperature_eq°C`

### 🚨 2. Détection d’anomalies
Mise en place de règles simples :
- Latence > 120 ms  
- Débit < 50 Mbps  
- Taux d’erreur > 2%  
- Température > 60°C  

Création d’une colonne `anomalie_detectee`.

### 🌡️ 3. Heatmap des anomalies
- Heatmap globale : anomalies par jour et par heure  
- Heatmap dédiée à l’antenne **A001**, permettant d’identifier les plages horaires critiques

### 🛰️ 4. Analyse par antenne
- Comptage des anomalies par antenne  
- Identification des antennes les plus instables  
- Analyse détaillée de **A001** (latence, débit, température)

### ⚖️ 5. Comparaison A001 vs A003
- Comparaison temporelle de la latence  
- Comparaison temporelle du débit  
- Mise en évidence d’une antenne saine vs une antenne saturée

---

## 🧠 Résultats principaux

### 🚨 L’antenne A001 est en surcharge chronique
- pics de latence jusqu’à 250 ms  
- chutes de débit sous 30 Mbps  
- taux d’erreur élevé  
- anomalies concentrées à certaines heures

### 🟢 A003 montre le comportement d’une antenne saine
- latence stable (40–70 ms)  
- débit régulier (80–110 Mbps)

### 🔥 Diagnostics formulés
- Surcharge radio en heures de pointe  
- Backhaul potentiellement insuffisant  
- Effet thermique secondaire  
- Recommandations :
  - ajout de capacités radio,
  - optimisation de paramètres réseau,
  - analyse de charge locale.

---

## 🧰 Technologies utilisées
- **Python**
- **pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- Jupyter Notebook

---

## 🚀 Prochaines améliorations
- Mise en place d’un modèle de détection d’anomalies (Isolation Forest)  
- Dashboard interactif (Streamlit)  
- Analyse géospatiale des antennes  

---

## 👤 Auteur
**Oumar Magassa**  
Master Mathématiques appliquées aux données – Paris 13  
Passionné par la data, les statistiques et les réseaux télécom.

---


