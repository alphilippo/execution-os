# Instructions push GitHub — execution-os

## Étape 1 — Créer le repo sur GitHub

1. Va sur https://github.com/new
2. Repository name : `execution-os`
3. Description : `An execution system skill for Claude — sprint planning, deep work, weekly rituals, and honest accountability`
4. Public ✅
5. **Ne coche PAS** "Add a README", ".gitignore", "Choose a license" (on les a déjà)
6. Clique "Create repository"

## Étape 2 — Push depuis ta machine

```bash
cd execution-os-github
git init
git add .
git commit -m "Initial release: execution-os v1.0 with 4 modules"
git branch -M main
git remote add origin https://github.com/<TON-USERNAME>/execution-os.git
git push -u origin main
```

## Étape 3 — Configurer le repo

Sur la page du repo :

1. **About** (côté droit, engrenage) :
   - Description : `Execution system skill for Claude — sprint planning, deep work, weekly rituals, accountability`
   - Topics : `claude`, `claude-skill`, `productivity`, `execution`, `deep-work`, `accountability`, `sprint-planning`, `ai-agent`
2. **Settings → Features** : désactive `Wiki`, laisse `Issues` actif

## Étape 4 — Lien avec thinking-os

Dans le README de `thinking-os`, ajoute une mention :
> **Related**: [execution-os](https://github.com/<ton-username>/execution-os) — execution system that composes well with thinking-os.

Et symétriquement dans le README de `execution-os`, ajoute :
> **Related**: [thinking-os](https://github.com/<ton-username>/thinking-os) — cognitive router that composes well with execution-os.

Ça crée un petit écosystème et renforce ton positionnement.

## Étape 5 — Amorcer la visibilité

Post LinkedIn/Twitter/X combiné :

> *"Je viens de publier 2 skills Claude open-source :*
> *— **thinking-os** : routeur cognitif, applique le bon framework de pensée (first principles, inversion, OODA, etc.) à chaque type de problème*
> *— **execution-os** : système d'exécution avec sprint planning, deep work, rétro hebdo, accountability honnête*
>
> *Elles se composent : thinking-os répond à QUOI faire, execution-os répond à COMMENT le faire.*
>
> *Apache 2.0, install en 2 commandes.*
>
> *[lien thinking-os] | [lien execution-os]"*

## Étape 6 — Monitoring

Check hebdo :
- Stars
- Issues
- Traffic source (Insights → Traffic)

Si une skill prend de la traction > l'autre, itère en priorité sur celle qui marche.
