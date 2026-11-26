# Entretien d'installation

À dérouler à la première utilisation du skill. Objectif : obtenir en une fois les paramètres qui conditionnent presque toutes les réponses de droit du travail, pour ne plus les redemander ensuite.

**Avant toute question** : chercher un fichier `profil.json` dans le dossier de travail (modèle : `profil.example.json` à la racine du skill). S'il existe, le lire et ne demander que les champs vides ou périmés.

## Comment mener l'entretien

- **Poser les questions par blocs, pas les 18 d'un coup.** Bloc 1 (identité de la situation) → puis bloc 2 (entreprise) → puis bloc 3 (contrat). Trois messages maximum.
- Utiliser l'outil de questions à choix multiples s'il est disponible : plus rapide sur mobile que de taper des réponses.
- Accepter « je ne sais pas ». Noter la case vide et indiquer où trouver l'information (bulletin de paie, contrat, extranet RH, base des conventions collectives).
- Ne pas bloquer : si l'utilisateur veut une réponse tout de suite, répondre avec ce qu'on a, en signalant explicitement ce qui reste conditionnel.

## Bloc 1 — Qui pose la question

1. **Vous êtes** : salarié·e / RH ou dirigeant·e / manager / représentant du personnel (CSE, DS) / conseil externe / autre.
2. **Vous intervenez pour** : votre propre situation / un salarié précis / un cadrage général de politique RH.
3. **Une procédure est-elle déjà engagée ?** Non / entretien préalable convoqué / notification faite / rupture conventionnelle en cours / contentieux ouvert / autre.
   → Si oui, demander **les dates** : elles font courir des délais impératifs.

## Bloc 2 — L'entreprise

4. **Effectif de l'entreprise** (et de l'établissement si différent) : moins de 11 / 11 à 49 / 50 à 249 / 250 à 999 / 1000 et plus.
   Les seuils commandent : obligations de représentation du personnel, procédure de licenciement économique, plancher du barème d'indemnités prud'homales, congé de reclassement, obligation de PSE.
5. **Convention collective applicable** : nom et si possible **IDCC** (numéro à 4 chiffres figurant sur le bulletin de paie).
   Si inconnu : le retrouver via l'outil officiel de recherche par SIRET (voir `sources-officielles.md`).
6. **Accords d'entreprise** en vigueur sur le sujet (temps de travail, rupture, indemnités de départ, télétravail, GEPP) — et où l'utilisateur peut les consulter.
7. **Instances** : CSE en place ? CSSCT ? Délégué syndical ? Date des dernières élections professionnelles ?
8. **Localisation** : France métropolitaine / **Alsace-Moselle** (régime local : préavis, jours fériés, maintien de salaire) / DROM.
9. **Secteur ou statut particulier** : association, portage salarial, intérim, groupement d'employeurs, particulier employeur, entreprise étrangère, salarié détaché ou expatrié.

## Bloc 3 — Le contrat concerné

10. **Type de contrat** : CDI / CDD (motif, terme précis ou imprécis, renouvellement) / intérim / apprentissage / contrat de professionnalisation / CDI de chantier / temps partiel / forfait jours.
11. **Date d'entrée** dans l'entreprise et **ancienneté reprise** éventuelle (reprise d'ancienneté contractuelle, transfert d'entreprise L1224-1, groupe).
12. **Statut et classification** : ouvrier / employé / technicien-agent de maîtrise / cadre / cadre dirigeant ; coefficient et position conventionnels.
13. **Rémunération** : brut mensuel, variable, primes (13e mois, ancienneté, objectifs), avantages en nature. Pour un calcul d'indemnité, demander les **12 derniers bulletins** ou les 3 derniers selon la formule retenue.
14. **Temps de travail** : temps plein / temps partiel (taux) / forfait jours (nombre) ; alternance temps plein–temps partiel au cours de la carrière (elle complique le calcul d'indemnité).
15. **Période d'essai** : durée, renouvellement prévu, dates.
16. **Clauses particulières** : non-concurrence (durée, périmètre, contrepartie), dédit-formation, mobilité, exclusivité, préavis contractuel.
17. **Situation du salarié** : mandat représentatif actuel ou récent, arrêt de travail en cours, inaptitude déclarée, grossesse ou congé familial, reconnaissance de travailleur handicapé, proximité de la retraite.
18. **Historique disciplinaire** : avertissements, mises à pied, dates (la prescription des faits fautifs court).

## Bloc 4 — Suite de la rupture (si une sortie est envisagée)

19. **Date de fin de contrat envisagée** — c'est elle, et non la date de signature, qui détermine le régime d'assurance chômage applicable.
20. **Âge du salarié à la sortie** — les durées maximales d'indemnisation varient par tranche d'âge.
21. **Indemnité supra-légale envisagée** — elle allonge le différé avant le premier versement de l'allocation.
22. **Antécédents d'indemnisation** — droits déjà ouverts, reliquat, droits rechargeables.

## Fiche profil à produire

Une fois l'entretien terminé, restituer une fiche courte et proposer de la conserver :

```markdown
# Profil droit du travail — [mis à jour le JJ/MM/AAAA]

## Contexte
- Rôle de l'utilisateur : …
- Entreprise : … salariés — établissement : …
- Convention collective : … (IDCC ….)
- Accords d'entreprise pertinents : …
- Instances : CSE … / DS … / dernières élections …
- Localisation : …

## Contrat de référence
- Type : … — début : … — ancienneté : …
- Statut/classification : …
- Temps de travail : …
- Rémunération de référence : …
- Clauses : …
- Situation particulière : …

## Points ouverts
- [ ] …
```

Ne pas y consigner de données sensibles inutiles : nom du salarié, état de santé détaillé, adresse. Une situation se décrit très bien sans identifier la personne.

## Sessions suivantes

Ouvrir par une confirmation en une ligne des paramètres qui comptent pour la question posée, et ne redemander que ce qui a pu changer (effectif, avenant de branche, nouvelle ancienneté). Si la question porte sur un autre salarié que celui du profil, refaire uniquement le bloc 3.
