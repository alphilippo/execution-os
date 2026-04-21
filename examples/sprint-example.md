# Exemple 1 — Sprint Planner appliqué

**Prompt utilisateur** :
> *"Je lance la cohorte 2 de mon programme startup dans 3 semaines. Il faut que je boucle le curriculum, que je setup la plateforme, que je recrute 10 mentors et que je valide 15 startups. Aide-moi à planifier."*

---

## Ce que la skill fait

**Détection** : signature "je lance X dans Y semaines" + "aide-moi à planifier" → `sprint-planner` immédiatement.

**Signal rouge à relever** : l'utilisateur liste 4 objectifs (curriculum + plateforme + mentors + startups). Le module doit **forcer la priorisation**.

---

## Sortie

⚙️ **Module : Sprint Planner**

Avant de planifier, une objection importante : tu as listé 4 livrables, c'est 3 de trop. Un sprint ne peut avoir qu'**une promesse centrale**. Si tu ne pouvais livrer qu'UNE chose avant J-0, laquelle rendrait les autres évidentes ?

**Ma lecture** : les 15 startups validées. Sans elles, pas besoin de curriculum spécifique, pas besoin de plateforme configurée, et les mentors ne peuvent pas matcher. Les startups validées débloquent tout le reste.

Plan proposé sur cette base :

# Sprint Plan — Cohorte 2 Launch Prep (J-21 → J-0)

## 🎯 Promesse unique
Valider 15 startups sélectionnées avec profil complet et engagement signé

## ⏱️ Budget
- Théorique : 120h sur 3 semaines (40h/sem)
- Réel (70%) : 84h

## 📍 Milestones

| # | Milestone | Temps estimé | Échéance | Dépendance |
|---|---|---|---|---|
| 1 | Critères de sélection écrits + grille de scoring | 4h | J-19 | Non |
| 2 | Open call lancé + pipeline de 50 candidatures | 8h | J-14 | Oui (audience) |
| 3 | Pré-sélection à 25 + interviews bookées | 10h | J-10 | Oui (dispo candidats) |
| 4 | Interviews réalisées + scoring final | 20h | J-5 | Oui (planning) |
| 5 | 15 startups validées + engagement signé | 12h | J-0 | Non |

**Total estimé** : 54h / 84h → 64% utilisation (sain — il reste du buffer)

## 📅 Allocation calendaire

### Semaine 1 (J-21 → J-14)
- **Lundi 9h-13h** : Deep work — critères de sélection + grille
- **Mardi 14h-18h** : Setup open call (landing, form, comms)
- **Mercredi matin** : Lancement open call + push communautés
- **Jeudi** : Buffer + premières review candidatures
- **Vendredi 9h-12h** : Review + push additionnel si pipeline < 50

### Semaine 2 (J-14 → J-7)
- **Lundi 9h-13h** : Pré-sélection à 25 (deep work scoring)
- **Mardi** : Booking interviews + comms aux non-retenus
- **Mercredi 9h-12h** : 3 interviews
- **Mercredi 14h-17h** : 3 interviews
- **Jeudi** : Buffer + interviews de rattrapage
- **Vendredi 9h-12h** : 3 interviews

### Semaine 3 (J-7 → J-0)
- **Lundi matin** : 3 interviews finales
- **Lundi 14h-17h** : Deep work — scoring final et délibération
- **Mardi** : Validation finale des 15, rédaction engagement
- **Mercredi** : Envoi des acceptations + relance signatures
- **Jeudi** : Buffer + relances
- **Vendredi** : Clôture des engagements

## 🚦 Critères & signaux

**Critère de succès** : 15 engagements signés au J-0, pipeline documenté pour la suite (curriculum + mentors).

**Signal de dérive à J+7** (fin semaine 1) : si pipeline < 40 candidatures, l'open call a échoué → urgence recrutement.

**Condition d'arrêt précoce** : si < 20 candidatures à J-14, repousser la cohorte de 2 semaines plutôt que valider des startups faibles.

## 🧨 Risques majeurs

1. **Pipeline trop faible** — mitigation : aligner 3 canaux de diffusion dès semaine 1 (communauté, partenaires, LinkedIn perso), pas 1 seul
2. **Startups validées qui ne signent pas** — mitigation : signature d'engagement DANS l'interview, pas après
3. **Temps interviews sous-estimé** — mitigation : format 45 min strict, buffer J+4 protégé

---

**Prochaine action concrète (dans les 2h)** : écrire les 5 critères de sélection et la grille de scoring — 30 min, livrable visible demain.

**Pour le curriculum, la plateforme et les mentors** : sprints suivants, à planifier après validation des 15 startups. Ne pas paralléliser, tu vas pourrir le cœur du programme.

⚠️ **Angle mort** : tu as peut-être sous-estimé le temps interviews. 45 min × 25 = 18h. Si chaque interview déborde à 60 min, tu es à 25h — ça bouffe ton buffer de semaine 2.

---

## Commentaires sur la sortie

Ce qui fait que cet exemple fonctionne :
1. Le module a **refusé** la liste de 4 livrables et forcé la priorisation
2. Le plan est **calendarisé avec heures précises**, pas des intentions
3. Jeudi reste **systématiquement libre** comme buffer
4. Les **dépendances externes sont nommées** et isolées
5. Les **risques ont des mitigations concrètes**, pas "être vigilant"
6. Une **prochaine action immédiate** est fournie — l'utilisateur peut démarrer dans les 2h
7. Les **3 autres livrables initiaux** sont renvoyés à des sprints ultérieurs, pas supprimés — c'est une priorisation, pas un refus

Ce qui manque volontairement :
- Pas de *"tu vas y arriver !"*
- Pas de détails sur le contenu du curriculum (hors scope de ce sprint)
- Pas d'outils Notion/Trello suggérés (le module est agnostique)
