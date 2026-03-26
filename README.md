# Dictionnaire du Permitting EnR — France

> Base de données structurée du processus d'autorisation des énergies renouvelables en France. 80 entités institutionnelles, 24 tags thématiques, export CSV / JSON.

🔗 **Accès direct** : [https://loiclebrec.github.io/dictionnaire-permitting-app/](https://loiclebrec.github.io/dictionnaire-permitting-app/)

---

## Fonctionnalités

- **80 entrées** pré-chargées couvrant les niveaux National, Régional, Départemental, Local, Législatif et Outils
- **24 tags thématiques** avec filtrage interactif
- **4 champs structurés** par entrée : Nature, Rôle permitting, Fondement juridique, Relations
- **Recherche plein texte** dans tous les champs
- **Export CSV** (séparateur configurable) et **JSON**
- **100% client-side** — fonctionne hors-ligne, aucune donnée transmise

## Tags thématiques

| Catégorie | Tags |
|---|---|
| **Processus** | consultation, décision, droit de veto, instruction, début du projet |
| **Thématique** | environnement, ICPE, urbanisme, énergie, patrimoine, foncier / espace |
| **Niveau géographique** | national, région, département, communauté de communes, commune |
| **Acteurs** | public, privé, gouvernance, participation citoyenne |
| **Autres** | planification, raccordement / réseau, contentieux / recours, financement |

## Structure des données

| Colonne | Description |
|---|---|
| `id` | Identifiant section (ex : `2.14`) |
| `niveau` | Niveau institutionnel |
| `chapitre` | Numéro de chapitre |
| `acronyme` | Sigle (ex : `DREAL`) |
| `nom_complet` | Dénomination complète |
| `titre_brut` | Titre complet tel qu'extrait |
| `nature` | Statut juridique |
| `role_permitting` | Rôle dans le processus d'autorisation |
| `fondement_juridique` | Base légale et réglementaire |
| `se_rapporte_a` | Entités en relation |
| `tags` | Tags thématiques (séparés par `;` en CSV) |

## Workflow VS Code (ajouter puis push)

Le fichier source des entrées est [entries.json](entries.json).

1. Ouvre [entries.json](entries.json) dans VS Code.
2. Ajoute/modifie tes entités (format JSON, tableau d'objets).
3. Recharge l'app: [index.html](index.html) charge `entries.json` en priorité.
4. Commit/push:

```bash
git add entries.json index.html README.md
git commit -m "Ajout de nouvelles entités"
git push
```

Notes:
- Si `entries.json` n'est pas disponible, l'app utilise les données embarquées dans [index.html](index.html).

## Source

Données extraites du *Dictionnaire du Processus de Permitting en France — Par niveau institutionnel* (PDF LaTeX, 106 pages).

## Licence

MIT — voir [LICENSE](LICENSE).
