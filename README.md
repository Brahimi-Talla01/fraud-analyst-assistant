# Fraud Analyst Assistant

> Détection de transactions frauduleuses (Mobile Money simulé) et assistant
> d'analyste qui explique les alertes, de la donnée au modèle déployé.

[badge CI] [badge licence code] [badge Python]

**Statut :** couche 1 en cours (semaine 1/4)

## Pourquoi ce projet

2 à 3 phrases : le problème (fraude très rare, deux types d'erreurs
aux coûts différents), l'approche, et ce que le projet démontre.

## Limites importantes

- Les données sont **synthétiques** (PaySim) et ne représentent pas des
  transactions réelles ni camerounaises.
- Le corpus de procédures de l'assistant est **fictif**, rédigé par l'auteur.
- Le champ « libellé » utilisé pour les tests d'injection est **inventé**.
- Ce n'est pas un système prêt pour la production.

## Aperçu de l'architecture

[schéma : données → validation → modèle → API → assistant (RAG + outils)]

## Démarrage rapide

```bash
git clone ...
cd fraud-analyst-assistant
cp .env.example .env
make data    # nécessite le CSV brut, voir docs/data.md
make train
make serve
curl -X POST http://localhost:8000/predict -d '{...}'
```

Prérequis : Python x.y, Docker.

## Résultats

| Modèle                     | PR-AUC | Rappel @ précision X % | Coût estimé |
| -------------------------- | ------ | ---------------------- | ----------- |
| (à compléter après mesure) |        |                        |             |

Hypothèses de coût et protocole : voir `docs/evaluation.md`.

## Structure du dépôt

Arborescence commentée (version courte).

## Tests et qualité

`make test`, ce que couvre chaque famille de tests, état de la CI.

## Décisions d'architecture

Liens vers les ADR (`docs/adr/`).

## Données

- Source : _Synthetic Financial Datasets For Fraud Detection_ (PaySim), E. A. Lopez-Rojas
- Lien : https://www.kaggle.com/datasets/ealaxi/paysim1
- Licence : CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/)
- Téléchargé le : … · SHA-256 : …
- Modifications apportées : validation, nettoyage, conversion en Parquet, features.
- Les données ne sont pas incluses dans ce dépôt.

## Assistant (couche 2)

Corpus, évaluation du retrieval, outils, permissions, résultats des tests
d'injection, lien vers la model card.

## Feuille de route

Ce qui reste à faire, y compris ce que tu as volontairement coupé.

## Licences

Code : MIT. Données : CC BY-SA 4.0 (voir ci-dessus).

## Citation

E. A. Lopez-Rojas, A. Elmir, S. Axelsson. « PaySim: A financial mobile money
simulator for fraud detection ». EMSS, Larnaca, Chypre, 2016.

## Auteur

Ibrahim Talla · LinkedIn · +237680331041
