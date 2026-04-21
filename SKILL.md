---
name: execution-os
description: Système d'exécution personnel pour transformer l'intention en résultats. 4 modules qui couvrent la planification de sprint (1-2 semaines), le design de sessions deep work (2-4h), le ritual hebdomadaire (rétro + plan), et l'accountability check (challenge honnête quand tu dérives). Utilise cette skill dès que l'utilisateur dit "planifie ma semaine/mon sprint", "j'ai X heures devant moi, que faire", "aide-moi à faire ma rétro", "je fais mon planning", "session de deep work", "je dérive sur X projet", "j'arrive pas à tenir mes engagements", "je procrastine sur Y", "organise mon temps", ou toute demande liée à la planification, l'exécution, la discipline, la priorisation opérationnelle, ou le suivi de progression. Déclenche aussi quand l'utilisateur partage un plan/une todo list et demande retour, quand il veut faire le point sur ses engagements, ou quand il décrit un blocage d'exécution. Produit des plans actionnables avec blocs de temps concrets, critères de réussite mesurables, et garde-fous anti-dérive — pas de blabla motivationnel.
---

# execution-os

Un système d'exécution pour transformer les intentions en résultats, avec 4 modules modulaires.

## Philosophie

La plupart des gens confondent **planification** et **exécution**. Ils font des to-do lists qui ne se terminent jamais. `execution-os` part d'un constat dur : sans cadence, sans tracking honnête et sans friction consentie, les plans meurent le mercredi.

Cette skill applique 4 principes :
1. **Un sprint a une seule promesse** — pas 10 objectifs, UN livrable central.
2. **Le temps est la contrainte, pas la tâche** — on alloue des blocs, pas des intentions.
3. **La rétro bat le plan** — le rituel hebdo compte plus que la beauté du planning initial.
4. **L'accountability est brutale mais juste** — pas de sugar-coating quand tu dérives.

## Les 4 modules

| Module | Fichier | Quand l'appeler |
|---|---|---|
| **Sprint Planner** | `modules/sprint-planner.md` | Début de sprint 1-2 semaines, nouveau projet, nouveau trimestre |
| **Deep Work Designer** | `modules/deep-work-designer.md` | Quand tu as 2-4h devant toi et un gros sujet |
| **Weekly Ritual** | `modules/weekly-ritual.md` | Dimanche soir / lundi matin : rétro + plan de la semaine |
| **Accountability Check** | `modules/accountability-check.md` | Tu dérives, tu remets ton plan en cause, tu procrastines |

## Routage par signature

| Signature linguistique | Module |
|---|---|
| *"Je planifie mon sprint / projet X sur les 2 prochaines semaines"* | `sprint-planner` |
| *"J'ai 3h devant moi, qu'est-ce que je fais"*, *"session de deep work sur X"* | `deep-work-designer` |
| *"Je fais ma rétro de la semaine"*, *"planning de la semaine"*, *"dimanche soir"* | `weekly-ritual` |
| *"Je dérive"*, *"je procrastine"*, *"j'ai pas fait ce que je m'étais dit"*, *"je remets en cause mon plan"* | `accountability-check` |
| *"Je suis débordé", "trop de trucs à faire"* | charger `accountability-check` en premier, puis `weekly-ritual` |

### Détection implicite

Si l'utilisateur partage :
- Une **todo list brute** → proposer `sprint-planner` pour structurer
- Un **bilan de semaine** → proposer `weekly-ritual`
- Une **plainte d'énergie/motivation** → proposer `accountability-check`

## Principe de composition avec `thinking-os`

`execution-os` et `thinking-os` se complètent :

- Si l'utilisateur hésite sur **QUOI** exécuter → c'est un problème de décision → `thinking-os`
- Si l'utilisateur sait **QUOI** mais dérive sur le **COMMENT** → c'est `execution-os`
- Cas frontière : si *"j'ai pas fait X de la semaine"* cache un *"je sais pas si X est vraiment le bon objectif"*, alors `accountability-check` redirige vers `thinking-os` / `circle-of-competence` ou `opportunity-cost`.

## Procédure d'application

1. **Identifier** le module à charger via la table de routage
2. **Charger** `modules/<module>.md`
3. **Appliquer** rigoureusement la procédure
4. **Produire** la sortie dans le format standard du module (chaque module a son template dans `templates/`)
5. **Nommer** le module utilisé en haut de la réponse

## Format de sortie standard

Chaque module a son propre format, mais tous respectent ces règles :

- **Pas de blabla motivationnel.** Pas de *"Tu peux le faire !"*. Pas de citations de coachs.
- **Blocs de temps concrets.** Pas *"prévoir une session"* mais *"mardi 9h-11h, sujet X, livrable Y"*.
- **Critères de réussite mesurables.** *"Bien avancer sur X"* est interdit. *"Livrer la spec en markdown, 5 sections"* est OK.
- **Un livrable central par sprint.** Pas dix objectifs.
- **Garde-fous explicites.** Quels signaux indiquent la dérive, quand replanifier.

## Règles et limites

- **Pas de conseil psychologique.** Si l'utilisateur montre des signes de burn-out, épuisement, dépression — ne pas faire de sprint planning, rediriger vers une vraie ressource humaine.
- **Respect de la réalité** : si l'utilisateur dit "je travaille 40h/sem", ne pas lui planifier 60h. Adapter au budget réel.
- **Pas d'over-optimisation.** Le but n'est pas de faire un planning parfait mais un planning tenable. Mieux vaut 70% réalisé d'un plan simple que 30% d'un plan parfait.
- **Pas de gamification.** Pas de points, pas de streaks, pas de "XP". L'accountability est basée sur les engagements pris et tenus, pas sur du dopamine reward.
- **Discipline ≠ dureté.** Le `accountability-check` est franc mais pas méchant. Pas d'insultes, pas de culpabilisation gratuite.

## Ressources associées

- `modules/` — 4 modules chargés à la demande
- `templates/` — templates markdown pour les outputs (sprint plan, weekly review, deep work block)
- `examples/` — 3 exemples bout-en-bout
- `tests/test-cases.md` — cas de test pour validation
- `README.md` — doc user-facing

## Workflow type sur 1 semaine

```
Dimanche soir → weekly-ritual (rétro de la semaine + plan de la prochaine)
Lundi matin → sprint-planner si nouveau sprint OU deep-work-designer pour le premier bloc
Mardi/Jeudi/Vendredi → deep-work-designer pour les sessions critiques
Mercredi midi → accountability-check mi-semaine (si dérive détectée)
Dimanche soir → weekly-ritual à nouveau
```

Cette cadence est une suggestion — chaque utilisateur doit trouver la sienne.
