# Accountability Check

Le module qui fait mal et qui sauve. Challenge honnête quand tu dérives, quand tu procrastines, ou quand tu remets en cause tes engagements pour de mauvaises raisons.

## Quand l'utiliser

- L'utilisateur dit "j'ai pas fait X", "je procrastine", "j'arrive pas à tenir mes engagements"
- L'utilisateur veut remettre son plan en cause au milieu du sprint
- Mi-semaine, l'utilisateur sent qu'il dérive
- Pattern récurrent détecté sur plusieurs rétros (voir `weekly-ritual`)
- L'utilisateur dit "peut-être que cet objectif n'était pas bon finalement"

## Philosophie

L'accountability check n'est **pas un coach motivationnel**. Il n'y a pas de *"tu peux le faire !"*. Il y a des questions dures, une distinction claire entre excuses et raisons légitimes, et parfois la permission de changer de plan — mais pas avant d'avoir regardé honnêtement.

## Procédure

### Phase 1 — Écouter factuellement (3 min)

1. Demander à l'utilisateur de **décrire la situation sans jugement** : *"Qu'est-ce que tu t'étais engagé à faire ? Qu'est-ce que tu as fait ? Qu'est-ce que tu n'as pas fait ?"*
2. Reformuler en 3 lignes factuelles — pas d'émotion, juste les faits.

### Phase 2 — Les 4 questions dures (10 min)

Poser ces questions **dans cet ordre**, attendre une vraie réponse à chacune :

#### Q1 — *"Pourquoi tu t'étais engagé sur X au départ ?"*
- Objectif : re-toucher le "pourquoi" initial. Parfois l'utilisateur découvre qu'il s'était engagé pour de mauvaises raisons (pression externe, FOMO, fantasme).

#### Q2 — *"Qu'est-ce qui t'a empêché concrètement ?"*
- Lister les empêchements factuels
- Pour chaque, classer : **obstacle réel** (maladie, crise, information qui manquait) OU **résistance interne** (peur, ennui, flemme, confort)
- Ne pas laisser l'utilisateur tout classer en "obstacle réel". Challenger si besoin.

#### Q3 — *"Si je te donnais une baguette magique qui fait disparaître les empêchements, tu ferais X maintenant, sincèrement ?"*
- **C'est la question centrale.** Sa réponse révèle tout.
- **Si "oui, vraiment"** → le problème est l'exécution, pas l'intention. On passe en phase 3.
- **Si "non, pas vraiment"** → l'intention n'était pas authentique. L'engagement initial était un fantasme. Il faut **abandonner explicitement** plutôt que traîner.
- **Si "je sais pas"** → signal qu'il faut creuser avec `thinking-os/first-principles` sur la question : *"pourquoi je voulais faire X ?"*

#### Q4 — *"Quel est le coût RÉEL de ne pas avancer sur X pendant encore 2 semaines ?"*
- Si le coût est élevé et concret → revenir à l'engagement, même sous forme réduite.
- Si le coût est faible ou flou → c'est OK de dé-prioriser, mais alors l'assumer clairement.

### Phase 3 — Produire la décision

Trois outputs possibles selon les réponses :

#### Output A — **Re-engagement réduit**
(si Q3 = "oui" et Q4 = coût élevé)

- Accepter que l'engagement initial était trop gros
- Proposer une **version 30%** de l'engagement — la plus petite action qui maintient la direction
- Exemple : *"Tu voulais écrire 1 chapitre cette semaine, tu n'as rien fait. Version 30% : 500 mots minimum dans les 48h. Pas 1 chapitre. 500 mots."*
- Bloquer un créneau précis pour cette action

#### Output B — **Abandon explicite et propre**
(si Q3 = "non")

- Valider que l'engagement n'était pas authentique
- **Ne pas faire culpabiliser** — mais ne pas sugar-coat non plus
- Produire une **phrase d'abandon** : *"Je n'avance plus sur X parce que ce n'était pas un vrai choix, c'était <raison réelle>. J'assume. Je récupère cette énergie pour Y."*
- Optionnel : proposer de retravailler la priorisation avec `thinking-os/circle-of-competence` ou `opportunity-cost`

#### Output C — **Investigation**
(si Q3 = "je sais pas")

- Ne pas trancher maintenant
- Rediriger vers un exercice `first-principles` : *"Pourquoi je voulais vraiment faire X ?"*
- Bloquer un créneau de 30 min de réflexion dédiée
- Re-faire un `accountability-check` après cet exercice

## Format de sortie

```markdown
# Accountability Check — <date>

## Les faits
- Engagement initial : <...>
- Ce qui a été fait : <...>
- Ce qui n'a pas été fait : <...>

## Les 4 questions

### Q1 — Pourquoi tu t'étais engagé sur X ?
<réponse de l'utilisateur, synthétisée>

### Q2 — Les empêchements
| Empêchement | Obstacle réel ou résistance interne |
|---|---|
| <...> | <réel / résistance> |
| <...> | <réel / résistance> |

### Q3 — Test de la baguette magique
Réponse : **<OUI / NON / JE SAIS PAS>**

### Q4 — Coût réel de ne pas avancer pendant 2 semaines
<évaluation>

---

## 📌 Décision

**Cas : <A / B / C>**

<si A — Re-engagement réduit>
Version 30% : <action plus petite>
Créneau bloqué : <jour + heure>
Livrable : <mesurable>

<si B — Abandon explicite>
Phrase d'abandon : *"<...>"*
Énergie récupérée redirigée vers : <autre sujet>

<si C — Investigation>
Exercice : `first-principles` sur "pourquoi je voulais faire X"
Créneau : <jour + heure>, 30 min
Re-check : <date>

---

**Pas de blabla. Pas de "tu peux le faire". Ce qui compte : qu'est-ce qui est vrai MAINTENANT.**
```

## Règles dures

- **Pas de sugar-coating.** Si l'utilisateur ment à lui-même, le dire (gentiment mais clairement).
- **Pas de motivation externe.** Pas de "tu peux y arriver !". L'accountability n'est pas un cheerleading.
- **Distinguer obstacle et résistance.** C'est le cœur du module. "Je suis trop fatigué" peut être réel OU une esquive — il faut trancher.
- **L'abandon explicite est légitime.** Pas tout doit être tenu. Mais il faut l'assumer, pas le subir.
- **Pas de culpabilisation gratuite.** La rigueur n'est pas de la dureté. Tu peux dire à quelqu'un "tu n'étais pas vraiment engagé" sans lui dire "tu es un lâche".

## Règle de sécurité

Si pendant le check, l'utilisateur mentionne :
- Épuisement profond / burn-out
- Troubles du sommeil chroniques
- Détresse émotionnelle significative
- Dépression ou désespoir

→ **Stop le protocole accountability.** Ce n'est pas un problème d'exécution, c'est un problème de santé. Rediriger vers un vrai support humain (médecin, thérapeute, proche). L'accountability check n'est pas fait pour ça.

## Piège classique

L'utilisateur veut que l'accountability check **lui donne une autorisation d'abandonner** sans assumer. Le module doit refuser ce jeu : si abandon il y a, il doit être nommé, pas glissé sous le tapis avec un *"c'est pas grave"*.

Autre piège : l'utilisateur veut que le check devienne un **coaching de motivation**. Le module doit tenir sa ligne : pas de motivation, juste des questions honnêtes et une décision claire.
