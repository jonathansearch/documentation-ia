# Chapitre 5 — Le Machine Learning (Apprentissage automatique)

> [← Retour au sommaire](../README.md)

---

## 5.1 Qu'est-ce que le Machine Learning ?

> « L'apprentissage automatique est le domaine d'étude qui donne aux ordinateurs la capacité d'apprendre **sans être explicitement programmés**. » — Arthur Samuel, 1959

Au lieu d'écrire des règles, on entraîne un modèle avec des **exemples**. Le modèle ajuste automatiquement ses paramètres pour minimiser ses erreurs.

### Analogie

Apprendre à un enfant à reconnaître un chien :
- ❌ On ne lui donne pas la règle « 4 pattes + 2 oreilles + une queue » (incomplète et rigide)
- ✅ On lui **montre plein de chiens** jusqu'à ce qu'il reconnaisse tout seul les motifs

C'est exactement ainsi que fonctionne le Machine Learning.

---

## 5.2 Les trois grands paradigmes

### 🏷️ 1. Apprentissage supervisé

Le modèle apprend à partir d'exemples **étiquetés** (chaque exemple vient avec la bonne réponse).

**Données** : (photo de mail → "spam") ou (photo de mail → "pas spam")

**Tâches principales** :
- **Classification** : prédire une catégorie (spam/pas spam, malade/sain, chat/chien)
- **Régression** : prédire une valeur numérique (prix d'une maison, température demain)

**Algorithmes courants** : régression linéaire/logistique, arbres de décision, forêts aléatoires, SVM, réseaux de neurones.

```
EXEMPLES ÉTIQUETÉS ──► ENTRAÎNEMENT ──► MODÈLE ──► NOUVELLE DONNÉE ──► PRÉDICTION
 (image, "chat")                          │
                                          ▼
                                     "C'est un chat (92% sûr)"
```

### 🧩 2. Apprentissage non supervisé

Les données **ne sont pas étiquetées** : le modèle doit découvrir seul des structures cachées.

**Tâches principales** :
- **Clustering (regroupement)** : segmenter automatiquement des clients en groupes homogènes
- **Réduction de dimension** : compresser l'information (utile pour visualiser)
- **Détection d'anomalies** : repérer les comportements inhabituels (fraude bancaire)

**Exemple** : une plateforme de streaming regroupe ses utilisateurs selon leurs goûts, sans savoir à l'avance quels groupes existent.

### 🎮 3. Apprentissage par renforcement

Un **agent** apprend par **essais et erreurs**, en recevant des récompenses ou des pénalités selon ses actions.

**Données** : pas d'exemples, mais un **environnement** et une fonction de récompense.

**Exemples** :
- **AlphaGo** : récompensé quand il gagne la partie
- **Robotique** : un bras robotisé récompensé quand il saisit l'objet
- **RLHF** : technique utilisée pour aligner les chatbots (comme ChatGPT) sur les préférences humaines

```
AGENT ──action──► ENVIRONNEMENT ──récompense/pénalité──► AGENT apprend
```

---

## 5.3 Tableau comparatif

| Critère | Supervisé | Non supervisé | Renforcement |
|---|---|---|---|
| Données | Étiquetées | Non étiquetées | Récompenses |
| Objectif | Prédire la bonne réponse | Découvrir des structures | Maximiser les récompenses |
| Exemple | Détection de spam | Segmentation clients | Jeu de Go, robotique |
| Analogie | Élève avec un professeur | Explorateur sans guide | Joueur qui tâtonne |

---

## 5.4 Exemple fil rouge : prédire le prix d'une maison à Yaoundé

Imaginons un modèle supervisé pour estimer le prix d'une maison :

**1. Données** (entraînement)：

| Surface | Quartier | Chambres | Prix réel |
|---|---|---|---|
| 120 m² | Bastos | 3 | 85M FCFA |
| 80 m² | Nkolbisson | 2 | 40M FCFA |
| 200 m² | Odza | 4 | 110M FCFA |
| ... | ... | ... | ... |

**2. Entraînement** : l'algorithme ajuste ses paramètres : « +500 000 FCFA par m², +15M si le quartier est Bastos... »

**3. Inférence** : nouvelle maison de 150 m² à Bastos, 4 chambres → le modèle prédit **~95M FCFA**.

**4. Évaluation** : on compare les prédictions aux prix réels de maisons jamais vues (ensemble de test).

---

## 5.5 Limites du Machine Learning

- 📉 **Dépendance aux données** : pas de bonnes données = pas de bon modèle
- ⚖️ **Biais** : un modèle apprend et amplifie les biais présents dans ses données
- 🔀 **Généralisation limitée** : un changement de contexte peut rendre le modèle obsolète
- 💰 **Coût** : collecte, nettoyage et calcul demandent temps et ressources

---

## ⬅️➡️ Navigation

[← Chapitre 4 — Types d'IA](04-types-ia.md) | [Chapitre 6 — Deep Learning →](06-deep-learning.md)
