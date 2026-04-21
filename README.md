# execution-os

> Système d'exécution personnel pour Claude : transforme l'intention en résultats, avec 4 modules modulaires (sprint planning, deep work, weekly ritual, accountability).

## Ce que ça fait

La plupart des gens confondent planification et exécution. Ils font des to-do lists qui ne se terminent jamais. `execution-os` applique 4 principes durs :

1. **Un sprint a une seule promesse** — pas 10 objectifs, UN livrable central
2. **Le temps est la contrainte, pas la tâche** — on alloue des blocs, pas des intentions
3. **La rétro bat le plan** — le rituel hebdo compte plus que la beauté du planning initial
4. **L'accountability est brutale mais juste** — pas de sugar-coating quand tu dérives

## Les 4 modules

| Module | Quand l'utiliser |
|---|---|
| **Sprint Planner** | Démarrer un sprint 1-2 semaines, nouveau projet, nouveau trimestre |
| **Deep Work Designer** | Quand tu as 2-4h devant toi et un gros sujet à avancer |
| **Weekly Ritual** | Dimanche soir / lundi matin, rétro + plan de la semaine |
| **Accountability Check** | Quand tu dérives, tu procrastines, tu remets en cause tes engagements |

## Déclencheurs

La skill se déclenche automatiquement quand tu dis :
- *"Planifie ma semaine / mon sprint"* → Sprint Planner
- *"J'ai 3h devant moi, que faire"* → Deep Work Designer
- *"Je fais ma rétro"*, *"Dimanche soir"* → Weekly Ritual
- *"Je dérive"*, *"Je procrastine sur X"*, *"J'arrive pas à tenir"* → Accountability Check

## Composition avec `thinking-os`

Si tu as aussi [thinking-os](https://github.com/alphilippo/thinking-os), les deux se complètent :
- `thinking-os` répond à la question **QUOI** faire
- `execution-os` répond à la question **COMMENT** le faire réellement

Si tu hésites sur quoi exécuter → utilise `thinking-os`.
Si tu sais quoi mais tu dérives sur comment → utilise `execution-os`.

## Installation

### Claude.ai

1. Télécharge/clone ce dossier
2. Upload dans `/mnt/skills/user/execution-os/`
3. La skill se déclenche automatiquement sur les prompts qui matchent

### Claude Code

```bash
cp -r execution-os ~/.claude/skills/
```

### API Claude

Package en `.skill` et upload via `/skills` endpoint.

## Exemples

### Sprint planning
> *"Je lance la cohorte 2 de mon programme dans 3 semaines, il faut boucler le curriculum, recruter 10 mentors, valider 15 startups."*

→ La skill **refuse** les 4 livrables, force à choisir UN (les 15 startups), produit un plan calendarisé avec buffer jeudi protégé.

### Deep work
> *"J'ai 3h devant moi, je veux avancer sur ma stratégie commerciale."*

→ La skill force un livrable observable (*"doc de 2 pages, 3 options comparées"*), découpe en blocs de 45-50 min avec pauses, impose le wrap-up.

### Weekly ritual
> *"Bilan de la semaine : j'ai pas fini mon gros livrable mais j'ai fait plein d'autres trucs."*

→ La skill **refuse** le "mais", chiffre le taux de livraison sur la promesse centrale (0%), identifie le pattern d'évitement, produit un plan qui attaque ce pattern.

### Accountability
> *"Ça fait 3 semaines que je dois écrire un livre, j'ai rien fait. Peut-être que c'est pas le bon moment ?"*

→ La skill **refuse** l'esquive, pose les 4 questions dures, distingue obstacle vs résistance interne, produit une décision claire (soit re-engagement à 30%, soit abandon explicite propre).

## Structure

```
execution-os/
├── SKILL.md                            # Métadonnées + routeur
├── README.md                           # Ce fichier
├── modules/
│   ├── sprint-planner.md
│   ├── deep-work-designer.md
│   ├── weekly-ritual.md
│   └── accountability-check.md
├── templates/                          # Templates markdown réutilisables
│   ├── sprint-plan-template.md
│   ├── weekly-ritual-template.md
│   └── deep-work-template.md
├── examples/                           # Exemples bout-en-bout
│   ├── sprint-example.md
│   ├── weekly-example.md
│   └── accountability-example.md
└── tests/
    └── test-cases.md                   # 11 cas de validation
```

## Philosophie

- **Progressive disclosure** : le SKILL.md ne contient que le routeur. Chaque module est chargé à la demande.
- **Pas de motivation gratuite** : pas de *"tu peux le faire !"*, pas de citations de coachs.
- **Priorité à la réalité** : pas d'over-optimisation, un plan tenable vaut mieux qu'un plan parfait.
- **Règle de sécurité** : si l'utilisateur montre des signes de burn-out / épuisement / détresse, la skill stoppe et redirige vers un vrai support humain.

## Limites

- Ne remplace pas un thérapeute, un coach humain, ni un médecin
- Ne fait pas de gamification (pas de points, pas de streaks)
- Les estimations temps restent des estimations — la skill ne fait pas de magie
- Ne fonctionne pas bien pour les tâches < 15 min (overhead > valeur)

## Roadmap

- **v1.0** (actuel) : 4 modules + 3 templates + routage
- **v1.1** : **Monthly ritual** (rétro + plan à l'échelle mensuelle)
- **v1.2** : **Energy tracking** plus fin (corrélation énergie / types de tâches)
- **v1.3** : **Composition explicite** avec `thinking-os` (redirection automatique)
- **v2.0** : **Mémoire des sprints passés** pour améliorer les estimations futures

## Licence

Apache 2.0 — fork, adapte, republie.

## Crédits

Conçu avec Claude comme Skill Architect. Inspiré par la tradition Cal Newport (deep work), Eisenhower (prioritization), Ray Dalio (principles), et la pratique Agile des sprints.
