# DIMENSIA — version simplifiée à 3 fichiers

Cette version contient exactement **3 fichiers à déposer à la racine de GitHub** :

- `app.py` — interface et tous les moteurs de calcul intégrés, avec jeux de données fictifs téléchargeables depuis la barre latérale.
- `requirements.txt` — dépendances Streamlit Cloud.
- `README.md` — ce guide.

## Déploiement Streamlit

1. Ouvrir le dépôt GitHub destiné à DIMENSIA.
2. Supprimer ou archiver les anciens fichiers et dossiers si nécessaire.
3. Déposer **les trois fichiers directement à la racine** du dépôt (ne pas mettre `app.py` dans un sous-dossier).
4. Sur Streamlit Community Cloud, sélectionner `app.py` comme fichier principal.
5. Attendre le redéploiement, puis ouvrir les logs en cas d'erreur.

## Lancement local

```bash
python -m pip install -r requirements.txt
python -m streamlit run app.py
```

## Portée scientifique

DIMENSIA est un outil **pédagogique** de calcul mécanique simplifié : poutres, semelles centrées, géométrie de sections, combinaisons à coefficients personnalisés, simulation probabiliste et import de données. Les jeux de données inclus sont **entièrement fictifs**. L'application ne fournit pas de dimensionnement réglementaire complet du béton armé selon BAEL ou Eurocode 2 et ne doit pas être utilisée seule pour concevoir un ouvrage.

## Pourquoi cette version ?

Les imports du type `from dimensia.mechanics import ...` ont été éliminés en intégrant les fonctions dans `app.py`. Cela évite l'erreur `ModuleNotFoundError` observée lorsque les fichiers étaient téléversés à plat dans GitHub.
