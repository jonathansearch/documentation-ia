# Chapitre 3 — Concepts fondamentaux

> [← Retour au sommaire](../README.md)

---

## 3.1 Les quatre piliers de l'IA moderne

Tout système d'IA moderne repose sur quatre éléments combinés :

```
   📊 DONNÉES  +  ⚙️ ALGORITHME  →  🧠 MODÈLE  →  🔮 PRÉDICTIONS
   (exemples)     (méthode)         (résultat)     (utilisation)
```

### 1. Les données (le carburant)

Les données sont les exemples fournis au système pour apprendre : photos, textes, relevés météo, historiques de ventes...

> 💡 **Règle d'or** : la qualité d'un modèle ne dépassera jamais la qualité de ses données. *(« Garbage in, garbage out »)*

### 2. L'algorithme (la méthode)

La recette mathématique utilisée pour extraire des motifs des données : régression, arbres de décision, réseaux de neurones...

### 3. Le modèle (le résultat)

Ce que l'on obtient après l'entraînement : un programme contenant des millions (voire milliards) de **paramètres** ajustés. C'est le modèle qu'on déploie et utilise.

### 4. L'inférence (l'utilisation)

Le moment où le modèle entraîné traite de **nouvelles données** jamais vues pour produire une prédiction, une classification ou une génération.

---

## 3.2 Le cycle de vie d'un projet IA

```
┌─────────────────┐
│ 1. Définir le   │
│    problème     │
└────────┬────────┘
         ▼
┌─────────────────┐
│ 2. Collecter &  │
│ préparer données│
└────────┬────────┘
         ▼
┌─────────────────┐
│ 3. Entraîner    │
│    le modèle    │
└────────┬────────┘
         ▼
┌─────────────────┐
│ 4. Évaluer les  │
│  performances   │
└────────┬────────┘
         ▼
┌─────────────────┐
│ 5. Déployer &   │
│    surveiller   │
└─────────────────┘
         ↑________│ (boucle d'amélioration continue)
```

| Étape | Objectif | Questions clés |
|---|---|---|
| **1. Problème** | Cadrer le besoin | Que veut-on prédire ou automatiser ? |
| **2. Données** | Réunir et nettoyer les exemples | Sont-elles fiables, représentatives, suffisantes ? |
| **3. Entraînement** | Ajuster les paramètres du modèle | Quel algorithme ? Combien de temps ? |
| **4. Évaluation** | Mesurer la qualité sur des données inédites | Précision acceptable ? Erreurs dangereuses ? |
| **5. Déploiement** | Mettre en production et surveiller | Le modèle dérive-t-il avec le temps ? |

---

## 3.3 Séparer les données : entraînement, validation, test

Pour éviter qu'un modèle apprenne « par cœur » (surapprentissage), on divise les données :

- **🎓 Ensemble d'entraînement (~70%)** — sert à apprendre.
- **🔍 Ensemble de validation (~15%)** — sert à régler les réglages (hyperparamètres).
- **📝 Ensemble de test (~15%)** — sert à mesurer la performance finale, comme un examen avec des questions inédites.

> ⚠️ **Surapprentissage (overfitting)** : un modèle qui obtient 99% sur ses données d'entraînement mais échoue dans le monde réel a appris par cœur au lieu de généraliser.

---

## 3.4 Mesurer la performance

Quelques métriques essentielles :

| Métrique | Question à laquelle elle répond |
|---|---|
| **Exactitude (accuracy)** | Quelle proportion de bonnes réponses ? |
| **Précision** | Parmi mes prédictions positives, combien sont correctes ? |
| **Rappel** | Parmi tous les vrais cas positifs, combien en ai-je détecté ? |
| **Erreur moyenne** | De combien le modèle se trompe-t-il en moyenne ? |

### Exemple : diagnostic médical
Un dépisteur de cancer doit avoir un **rappel élevé** : mieux vaut des fausses alertes qu'un cancer manqué. À l'inverse, un filtre anti-spam privilégie la **précision** pour ne pas supprimer d'emails importants.

---

## 3.5 L'IA n'est pas de la magie

À retenir absolument :

- Un modèle IA produit des **probabilités**, pas des certitudes.
- Il ne « comprend » pas au sens humain : il calcule des **corrélations statistiques**.
- Il est **spécialisé** : un modèle entraîné à reconnaître des chats ne sait rien faire d'autre.
- Il peut être **biaisé** si ses données d'entraînement l'étaient (voir [chapitre 8](08-ethique.md)).

---

## ⬅️➡️ Navigation

[← Chapitre 2 — Histoire](02-histoire.md) | [Chapitre 4 — Les types d'IA →](04-types-ia.md)
