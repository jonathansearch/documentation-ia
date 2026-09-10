# Chapitre 6 — Le Deep Learning (Apprentissage profond)

> [← Retour au sommaire](../README.md)

---

## 6.1 Qu'est-ce que le Deep Learning ?

Le **Deep Learning** est une branche du Machine Learning utilisant des **réseaux de neurones artificiels profonds**, vaguement inspirés du cerveau humain. C'est la technologie derrière la quasi-totalité des percées récentes de l'IA.

```
INTELLIGENCE ARTIFICIELLE
└── MACHINE LEARNING
    └── DEEP LEARNING
        └── IA GÉNÉRATIVE (LLM, diffusion...)
```

---

## 6.2 Le neurone artificiel

Un neurone artificiel est une fonction mathématique simple :

1. Il reçoit des **entrées** (nombres)
2. Il les multiplie par des **poids** (appris pendant l'entraînement)
3. Il applique une **fonction d'activation**
4. Il produit une **sortie**, transmise aux neurones suivants

```
   x1 ──(poids w1)──┐
   x2 ──(poids w2)──┼──[ Σ + activation ]──► sortie
   x3 ──(poids w3)──┘
```

Seul, un neurone ne sait presque rien faire. Mais **des milliards de neurones connectés en couches** peuvent représenter des fonctions d'une complexité stupéfiante — c'est toute la puissance du Deep Learning.

---

## 6.3 Architecture d'un réseau profond

```
ENTRÉES          COUCHES CACHÉES            SORTIE
                 (d'où le terme "profond")

  ○ ────►  ○  ○  ○  ○ ────► ○  ○  ○ ────► 🐱 chat ?
  ○ image  ○  ○  ○  ○       ○  ○  ○       🐶 chien ?
  ○ ────►  ○  ○  ○  ○ ────► ○  ○  ○ ────► 🚗 voiture ?
```

| Couche | Rôle (exemple : reconnaissance d'images) |
|---|---|
| **Entrée** | Reçoit les pixels bruts |
| **Couches basses** | Détectent les contours, les couleurs |
| **Couches moyennes** | Assemblent des formes (yeux, oreilles, roues) |
| **Couches hautes** | Reconnaissent des concepts (visage, animal) |
| **Sortie** | Produit la décision finale (probabilités) |

### Comment apprend-il ?

La **rétropropagation** (backpropagation) : à chaque erreur de prédiction, l'algorithme calcule la « responsabilité » de chaque poids et l'ajuste légèrement dans la bonne direction. Répété des millions de fois, ce processus simple produit un modèle très performant.

---

## 6.4 Les grandes familles d'architectures

### 🖼️ CNN — Réseaux convolutifs (1989, popularisés en 2012)
Spécialistes de l'**image**. Ils parcourent l'image avec de petits filtres détectant des motifs locaux.
- Applications : reconnaissance faciale, imagerie médicale, véhicules autonomes

### 🔁 RNN / LSTM — Réseaux récurrents (années 1990)
Conçus pour les **séquences** (texte, audio, séries temporelles), avec une forme de mémoire.
- Applications : traduction automatique, reconnaissance vocale (avant les Transformers)

### ⚡ Transformers (2017) — l'architecture dominante
Révolution basée sur le mécanisme d'**attention** : le modèle apprend à « regarder » les parties pertinentes du contexte, quelle que soit leur distance.
- Applications : GPT, Claude, Gemini, BERT, traduction, génération de texte, d'images et de code
- Avantages : traitement parallèle (rapide) et excellente gestion du contexte long

### 🎨 Modèles de diffusion (2020+)
Apprennent à **générer des images** en partant de bruit aléatoire et en le « débruitant » progressivement.
- Applications : DALL-E, Midjourney, Stable Diffusion

---

## 6.5 Les grands modèles de langage (LLM)

Les **LLM** (Large Language Models) sont des Transformers entraînés sur d'immenses corpus de texte pour prédire le mot suivant.

### Ce simple objectif produit des capacités étonnantes

En apprenant à prédire « le mot qui suit », le modèle acquiert implicitement :
- des connaissances factuelles du monde
- la grammaire de centaines de langues
- des capacités de raisonnement, de traduction, de résumé, de codage...

### Chiffres qui donnent le vertige

| Élément | Ordre de grandeur |
|---|---|
| Paramètres | Des milliards à des centaines de milliards |
| Données d'entraînement | Une bonne partie du web public |
| Coût d'entraînement | Jusqu'à plusieurs dizaines de millions de dollars |
| Durée | Des semaines/mois sur des milliers de GPU |

### Le pipeline d'un chatbot moderne

1. **Pré-entraînement** — le modèle lit internet et apprend la langue et le monde
2. **Affinage supervisé (SFT)** — on lui apprend à répondre comme un assistant
3. **Alignement (RLHF/préférences)** — des évaluateurs humains l'orientent vers des réponses utiles, exactes et sûres

---

## 6.6 Forces et limites du Deep Learning

### ✅ Forces
- Performances état de l'art sur image, son, langue
- S'améliore avec plus de données et de calcul (*lois d'échelle*)
- Polyvalent : une même architecture pour beaucoup de tâches

### ❌ Limites
- Énergivore et coûteux
- Opacité : difficile d'expliquer une décision (*boîte noire*)
- Hallucinations : peut générer de fausses informations avec aplomb
- Fragile hors de son domaine d'entraînement

---

## ⬅️➡️ Navigation

[← Chapitre 5 — Machine Learning](05-machine-learning.md) | [Chapitre 7 — Applications →](07-applications.md)
