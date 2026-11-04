# Bottleneck — amélioration du projet 6 (comparaison notebook personnel / notebook IA)

Mission : améliorer le notebook du projet 6 avec l'aide d'une IA, de façon **critique et documentée**
(comparer au moins 2 options, justifier par des critères, conserver des traces).

Auteure : Luu Nguyen Minh Huyen — Data Analyst — 02/2026

## Contenu du dossier
| Fichier | Rôle |
|---|---|
| `Luu_Minh_Huyen_1_notebook_022026_1_corrige_IA.ipynb` | **Livrable principal** : ton notebook (version `_1`) corrigé sur place, avec 20 commentaires « critique et documenté » |
| Dossier « Amélioration du projet 6 » (document en ligne) | Synthèse, veille, cahier des charges, pilotage, traçabilité IA, limites, reproductibilité |
| `Luu_Minh_Huyen_3_pilotage_et_veille_022026.xlsx` | Veille, cahier des charges (KPI), formation, backlog, Kanban, planning, risques, journal des essais IA |
| `corrige_IA_sorties/` | Export Excel de la table propre, tableau de synthèse personnel / IA, graphiques |
| `requirements.txt` | Versions des bibliothèques |

Les fichiers `projet6_*`, `bottleneck_donnees_propres.xlsx`, `Luu_Minh_Huyen_1_notebook_022026_v2.ipynb` et `v2_sorties/` viennent des étapes précédentes et ne font pas partie de la mission en cours.

## Repères dans le notebook
- `# [PERSONNEL v1]` : ton code d'origine, conservé en commentaire
- `# [CORRIGÉ IA]` : cellule corrigée sur place (19 cellules), raison en première ligne
- `# [IA]` : cellule ajoutée (18 cellules) : variante, test, comparaison
- 🔎 « Critique et documenté » : commentaire après chaque requête (options, critères, traces, décision)

## Exécuter le notebook
1. Python 3.12 puis `pip install -r requirements.txt` (et `plotly` si tu veux voir tes graphiques interactifs).
2. Placer `erp.xlsx`, `liaison.xlsx`, `web.xlsx` dans un dossier `datasets/` à côté du notebook.
3. Exécuter toutes les cellules (environ 20 secondes). La dernière cellule de tests s'arrête sur une erreur si un test échoue.

## Reproductibilité
- Graine unique `SEED = 42` ; benchmark sur 30 graines.
- Plus de chemin absolu ni de `%pip install`.
- Testé avec Python 3.12.3, pandas 3.0.2 (compatibilité pandas 2.x prévue, non testée).

## Hypothèses à valider
- `price` (ERP) = prix HT (paramètre `PRIX_EST_TTC`) ; `total_sales` = ventes d'octobre.
- Seuil de la règle de prix : facteur 1,5 autour de la médiane de la catégorie.

## RGPD
Aucune donnée personnelle dans les trois fichiers ; `post_author` n'est pas conservée ; le test T7 vérifie l'absence de colonne personnelle dans l'export.
