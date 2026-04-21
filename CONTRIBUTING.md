# Contributing to execution-os

Merci de vouloir contribuer. `execution-os` est une skill Claude open-source — les contributions les plus utiles améliorent les **modules existants** ou ajoutent de nouveaux **rituels d'exécution** rigoureusement définis.

## Les 3 types de contributions bienvenues

### 1. Amélioration des modules existants

Si tu constates que :
- Le `sprint-planner` laisse passer trop d'objectifs
- Le `deep-work-designer` n'identifie pas bien l'obstacle #1
- Le `weekly-ritual` sugar-coat la rétro
- L'`accountability-check` ne détecte pas la résistance déguisée en obstacle

Ouvre une issue avec le prompt exact qui a causé l'échec + la sortie obtenue + ta proposition d'amélioration.

### 2. Nouveaux modules

On peut ajouter un module si :
- **Unique** : il ne fait pas doublon avec les 4 existants
- **Rigoureux** : il impose des contraintes, pas des suggestions
- **Testable** : on peut écrire 5+ cas de test pour valider ses sorties

Candidats bienvenus :
- **Monthly Ritual** (sur le modèle du weekly mais plus large)
- **Project Kickoff** (premier jour d'un nouveau projet)
- **Decision Log** (tracker décisions prises et leur issue)
- **Time Audit** (où part vraiment mon temps)

Candidats **refusés** :
- Pomodoro timer (trop simple, existe partout)
- Goal setting générique (trop vague, pas actionnable)
- Gamification / streaks (contraire à la philosophie)

### 3. Templates et exemples

Plus on a d'exemples concrets variés (consultant, founder, salarié, créateur), mieux la skill se déclenche correctement.

## Ce qu'on refuse

- Motivation gratuite ("tu peux le faire !")
- Citations de coachs/gourous non-nécessaires
- Gamification avec points/XP/streaks
- Surcharge de frameworks (on veut rester à 4-6 modules max)

## Style

- **Ton direct**, pas de sugar-coating
- **Livrables observables** (pas "avancer sur X")
- **Heures précises** (pas "mardi matin")
- **Garde-fous explicites** (quels signaux pour replanifier)

## Process

1. Fork le repo
2. Branche `feat/<module>` ou `fix/<problème>`
3. Ajoute au moins 3 cas de test dans `tests/test-cases.md`
4. Commit clair : `feat: add monthly-ritual module`
5. PR avec description + sortie d'exemple

## Code de conduite

Soyez rigoureux avec les idées, gentils avec les personnes. Les débats sont bienvenus, les attaques personnelles non.
