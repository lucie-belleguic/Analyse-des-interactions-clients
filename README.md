# 🤖 **Analyse des interactions clients**

## *Prédiction du sentiment associé à un tweet et mise en place d’une démarche MLOps*

Bienvenue dans mon projet **Analyse de Sentiments**, réalisé dans le cadre de ma formation en Data Science.  
L’objectif était de **prédire le sentiment associé à des tweets** (positif ou négatif) et de mettre en place une **chaîne complète de traitement et de déploiement** en respectant les bonnes pratiques MLOps.

---

## 🚀 Fonctionnalités principales

- 📊 Prétraitement avancé du texte (normalisation, lemmatisation, suppression des stopwords, etc.)
- 🔎 Comparaison de plusieurs approches :
  - **Régression Logistique** (TF-IDF)
  - **RNN LSTM** (Word Embeddings)
  - **RoBERTa** (Transformers pré-entraînés)
- ⚖️ Évaluation des performances avec métriques et visualisations
- 🔧 Suivi et monitoring du modèle via **MLflow**
- 🚀 Mise en production avec un pipeline de déploiement continu : Déploiement automatisé avec **GitHub Actions** et hébergement sur **Azure**
- 📈 Supervision et alertes automatiques en cas de dérive des performances

---

## 🧰 Stack technique

- **Python**
- **Scikit-learn**, **PyTorch**, **TensorFlow**
- **Transformers (Hugging Face)**
- **MLflow** pour le suivi des expériences
- **GitHub Actions** pour l’intégration et le déploiement continus (CI/CD)
- **Azure** pour l’hébergement du modèle et de l’API

---

## 🛠️ Installation

1. **Cloner le dépôt**

```bash
git clone https://github.com/lucie-belleguic/analyse-sentiments.git
cd analyse-sentiments
```

2. **Installer les dépendances**

```bash
pip install -r requirements.txt
```

3. **Entraîner un modèle**

```bash
python train.py
```

4. **Lancer l’API en local (optionnel)**

```bash
python app.py
```

---

## 🎮 Utilisation

### Exemple d’appel à l’API

```bash
curl -X POST "http://localhost:5000/predict" -H "Content-Type: application/json" -d '{"text": "J’adore ce produit !"}'
```

Réponse attendue :  

```json
{"sentiment": "positif"}
```

---

## 📁 Structure du projet

```
analyse-sentiments/
├── data/                    # Jeux de données
├── models/                  # Modèles sauvegardés
├── notebooks/               # Notebooks exploratoires
├── app.py                   # API pour l’inférence
├── train.py                 # Script d’entraînement
├── requirements.txt         # Dépendances Python
├── .github/workflows/       # Pipelines CI/CD (GitHub Actions)
├── README.md                # Fichier de présentation du projet
├── LICENSE                  # Fichier de licence (MIT)
└── docs/
    └── Presentation.pdf     # Présentation du projet
```

---

## 📊 Résultats

- **Régression Logistique (TF-IDF)** : simple, rapide, mais peu contextuel  
- **RNN LSTM (Word Embeddings)** : contextuel, mais lent et moins performant  
- **RoBERTa** : meilleur compromis performance/précision, retenu pour le déploiement  

---

## 🚀 Déploiement

- **Intégration continue (CI/CD)** : GitHub Actions exécute automatiquement les tests et la mise à jour du modèle.  
- **Hébergement** : l’API est déployée sur **Azure**, rendant le modèle accessible via une API REST.  
- **Monitoring** : suivi des performances et alertes automatiques en cas de dérive.

---

## 🔭 Développement futur

Améliorations possibles :
- Extension à d’autres langues
- Optimisation des coûts d’inférence
- Intégration d’un système de détection de dérive des données

---

## 🎓 Contexte

Ce projet a été développé dans le cadre de ma formation en Data Science.  
Il démontre :  
- La mise en œuvre de techniques modernes de NLP (TF-IDF, Word Embeddings, Transformers)  
- La comparaison de modèles de complexité croissante  
- L’intégration d’une démarche complète de mise en production (MLOps) avec **Azure** et **GitHub Actions**

---

## 📄 Licence

Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.
