# Sprint Planner

Planifie un sprint de 1-2 semaines à partir d'un objectif, en produisant un plan qui tient vraiment.

## Quand l'utiliser

- Début de sprint (1 à 2 semaines)
- Nouveau projet qui démarre
- Nouveau trimestre / nouveau mois
- L'utilisateur dit "je planifie les 2 prochaines semaines", "je démarre X", "mon sprint sur Y"

## Procédure

### Phase 1 — Cadrer la promesse (5 min)

1. **Demander** : *"Quel est le livrable UNIQUE du sprint ?"* — une seule chose, pas trois.
2. Si l'utilisateur liste plusieurs objectifs → forcer la priorisation : *"Si tu ne pouvais livrer qu'UN seul à la fin du sprint, lequel ?"* Les autres deviennent du "nice to have".
3. **Reformuler le livrable** en une phrase commençant par un verbe d'action + résultat observable.
   - ❌ *"Avancer sur le produit"*
   - ✅ *"Livrer le flow de signup fonctionnel avec 3 providers OAuth"*

### Phase 2 — Estimer le budget temps (5 min)

4. **Demander** : *"Combien d'heures réelles tu peux allouer ce sprint ?"*
5. **Appliquer la règle du 70%** : le budget réel disponible = heures théoriques × 0.7 (buffer pour urgences, réunions, imprévus).
6. Exemple : 40h théoriques → 28h réelles pour le sprint.

### Phase 3 — Décomposer (15 min)

7. Lister les **milestones** qui mènent au livrable — 3 à 5 jalons maximum.
8. Pour chaque milestone, estimer le temps en heures (pas en jours — trop imprécis).
9. **Somme totale** des estimations. Si > 80% du budget réel → le scope est trop gros, couper.
10. Identifier les **dépendances externes** (validation d'un tiers, API, livraison d'un autre) — les isoler, elles sont les #1 risques de retard.

### Phase 4 — Allouer dans le calendrier (10 min)

11. Bloquer des **plages dédiées** dans un calendrier théorique (jour + créneau horaire).
12. Règle : au moins **2 sessions de deep work de 2-3h** par semaine pour le travail cognitif lourd.
13. Les tâches légères (comms, admin, review) → plages courtes (30-60 min) en matinée ou fin de journée.
14. **Jeudi après-midi = buffer non-alloué** pour absorber les dérives.

### Phase 5 — Définir les signaux (5 min)

15. **Critère de succès** : qu'est-ce qui sera vrai en fin de sprint si c'est réussi ? (mesurable)
16. **Signal de dérive à mi-sprint** : quel pourcentage de progression attendu à J+5 ?
17. **Condition d'arrêt précoce** : à quelle condition tu arrêtes le sprint et tu re-planifies ?

## Format de sortie

```markdown
# Sprint Plan — <nom du sprint> (<dates>)

## 🎯 Promesse unique
<livrable en une phrase, avec verbe d'action>

## ⏱️ Budget
- Théorique : <X>h
- Réel (70%) : <Y>h

## 📍 Milestones

| # | Milestone | Temps estimé | Échéance | Dépendance |
|---|---|---|---|---|
| 1 | <...> | <N>h | <jour> | <externe ou non> |
| 2 | <...> | <N>h | <jour> | <...> |
| 3 | <...> | <N>h | <jour> | <...> |

**Total estimé** : <Z>h / <Y>h budget → <X%> utilisation

## 📅 Allocation calendaire (vue théorique)

### Semaine 1
- **Lundi 9h-11h** : Deep work sur <milestone 1>
- **Lundi 14h-15h** : Comms, emails
- **Mardi 9h-12h** : Deep work sur <milestone 1>, livraison
- **Mercredi 9h-11h** : Deep work sur <milestone 2>
- **Mercredi 14h** : <validation ou rendez-vous>
- **Jeudi** : Buffer non-alloué (absorbe les dérives)
- **Vendredi 9h-11h** : Deep work sur <milestone 2>

### Semaine 2
<...>

## 🚦 Critères & signaux

**Critère de succès** : <mesurable, en fin de sprint>

**Signal de dérive à J+5** : <X>% de <milestone N> complété. Si moins → alerter.

**Condition d'arrêt précoce** : si <événement clair> → stopper, reprendre en `accountability-check`.

## 🧨 Risques majeurs

1. **<risque 1>** — mitigation : <action préventive>
2. **<risque 2>** — mitigation : <action préventive>
3. **<risque 3>** — mitigation : <action préventive>

---

**Prochaine action concrète** (à faire dans les 2h) : <action spécifique qui lance le sprint>
```

## Règles dures

- **Un seul livrable central.** Si l'utilisateur résiste et veut absolument plusieurs objectifs, produire 2 sprint plans séquentiels, pas parallèles.
- **Pas de tâches < 15 min dans le plan.** Elles sont agrégées en blocs de "comms/admin".
- **Jeudi reste libre.** Ne pas négocier là-dessus — c'est le buffer qui sauve le sprint.
- **Dépendances externes isolées.** Elles ne doivent pas être sur le chemin critique si on peut l'éviter.
- **Le plan doit tenir sur une page.** Si ça déborde, c'est qu'il y a trop de scope.

## Piège classique

L'utilisateur arrive avec 10 objectifs et veut "tout caser". Le rôle du module est de **refuser** poliment et de forcer le choix. Un sprint bien cadré à 1 promesse bat 10 promesses non tenues.
