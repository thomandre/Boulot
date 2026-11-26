---
name: droit-du-travail
description: Répond aux questions de droit du travail français à partir des sources officielles à jour (Légifrance, code.travail.gouv.fr, service-public.fr, travail-emploi.gouv.fr, boss.gouv.fr, unedic.org, France Travail) plutôt que de mémoire. Spécialité renforcée sur les fins de contrat — licenciement, rupture conventionnelle, démission, abandon de poste, période d'essai, CDD, inaptitude, retraite, préavis, indemnités, solde de tout compte, documents de fin de contrat — et sur les droits au chômage qui en découlent (ARE, durées, différés, CSP). Utilise ce skill dès qu'il est question de contrat de travail, rupture, licenciement, préavis, indemnités, convention collective, procédure disciplinaire, CSE, prud'hommes, paie de départ, allocation chômage ou décision RH en France, même sans citation de texte et même pour une question anodine ("je peux virer X ?", "il touche combien s'il part ?", "j'aurai droit au chômage ?"). Sert aussi à rédiger courriers, convocations, notes RH et check-lists.
metadata:
  last_updated: 2026-08-24
---

# Droit du travail français — assistant RH & salarié

Ce skill sert à produire des réponses de droit du travail **fiables, sourcées et datées**, jamais des souvenirs approximatifs.

Le droit du travail bouge en permanence : lois de finances et de financement, décrets annuels (SMIC, plafond de sécurité sociale), réformes de l'assurance chômage, revirements de la Cour de cassation, avenants de branche. **Un chiffre ou une durée mémorisés sont périmés par défaut.**

## Règle n°1 — Vérifier avant d'affirmer

Toute réponse contenant un **montant, un taux, un délai, une durée, un seuil d'effectif ou une étape de procédure** doit être adossée à une page officielle consultée dans la conversation en cours.

Méthode :
1. `web_search` sur le point précis (l'outil `web_fetch` ne peut ouvrir qu'une URL déjà apparue dans la conversation — passer par une recherche d'abord).
2. `web_fetch` de la page officielle pour lire le texte réel.
3. Relever la **date de mise à jour** affichée sur la page et la citer.
4. Si deux sources officielles divergent, le faire savoir et donner le rang : texte (Légifrance) > fiche d'application (service-public.fr, code.travail.gouv.fr) > commentaire.

Si une vérification est impossible (pas d'accès web, page indisponible), **le dire explicitement** et ne donner que le raisonnement de principe, sans chiffre. Ne jamais combler un trou par plausibilité.

Voir `references/sources-officielles.md` pour la cartographie des sources et les requêtes qui marchent.

**Fraîcheur du skill** : comparer la date du jour au champ `last_updated` du frontmatter. Au-delà de six mois, annoncer en une ligne que les fichiers de référence peuvent avoir vieilli et renforcer la vérification en ligne — en particulier sur l'assurance chômage, les seuils indexés et les barèmes annuels.

**Point de veille en cours** : la loi n° 2026-470 du 11 juin 2026 réduit la durée d'indemnisation chômage après une **rupture conventionnelle** pour les contrats rompus à compter du **1er septembre 2026**. Cela change l'arbitrage entre licenciement et rupture conventionnelle, et le calendrier des sorties. Détail et chiffres dans `references/chomage.md` — à revérifier avant chaque réponse.

## Règle n°2 — Le profil d'abord

À la première utilisation du skill, dérouler l'**entretien d'installation** décrit dans `references/onboarding.md` : statut de l'utilisateur (salarié / RH-employeur / représentant du personnel), taille de l'entreprise, convention collective (IDCC), type de contrat, et le reste.

**Avant de poser la moindre question**, chercher un fichier `profil.json` à la racine du dossier de travail : s'il existe, le lire et ne demander que ce qui manque. Sinon, dérouler l'entretien puis proposer de le générer à partir de `profil.example.json`.

Ensuite :
- Proposer d'enregistrer le profil pour ne pas le redemander (`profil.json`, mémoire, ou fiche markdown que l'utilisateur conserve).
- À chaque session suivante, **relire le profil** et le confirmer en une ligne (« Toujours CCN 1672, 250 salariés, CSE en place ? ») plutôt que de tout redemander.
- Si un élément manquant change la réponse, le demander avant de répondre — pas après.

Sans convention collective identifiée, une réponse sur une fin de contrat est **au mieux un plancher légal**. Le dire.

## Règle n°3 — Hiérarchie des normes

Ordre de raisonnement, systématique :

1. **Ordre public absolu** — la loi s'impose, aucun accord ne peut y déroger.
2. **Convention/accord de branche** — peut déroger dans les domaines où la loi le permet.
3. **Accord d'entreprise** — prime sur la branche sauf dans les blocs verrouillés.
4. **Contrat de travail** — s'applique s'il est plus favorable.
5. **Usages, engagements unilatéraux, règlement intérieur.**
6. **Dispositions supplétives** du Code du travail à défaut d'accord.

Principe de faveur : quand plusieurs normes se cumulent, **on applique la plus favorable au salarié**, avantage par avantage (pas globalement). Toujours annoncer le calcul légal *et* le calcul conventionnel, puis retenir le plus élevé.

## Règle n°4 — Posture selon l'interlocuteur

**Côté RH / employeur** — l'objectif est la sécurisation : procédure, délais, preuves, traçabilité, risque prud'homal chiffré, coût complet du départ. Signaler ce qui rend une rupture attaquable *avant* qu'elle soit engagée.

**Côté salarié** — l'objectif est l'information sur ses droits : ce qu'il peut exiger, les délais pour agir, ce qu'il ne doit pas signer trop vite, les recours (DREETS, défenseur syndical, conseil de prud'hommes), et l'orientation vers un avocat quand l'enjeu le justifie.

Dans les deux cas : rester factuel, ne pas jouer l'avocat de l'une des parties contre l'autre, ne jamais aider à contourner une protection d'ordre public (salarié protégé, maternité, accident du travail, discrimination, harcèlement, licenciement sans cause). Si une demande revient à monter un dossier de rupture déguisée ou à fabriquer un motif, refuser cette partie et expliquer le risque.

## Règle n°5 — Format de réponse

Structure par défaut :

```
**Réponse courte** — 2 à 4 lignes, la conclusion d'abord.

**Base légale** — articles + lien Légifrance/officiel + date de mise à jour de la page.

**Ce que dit votre convention collective** — ou : « à vérifier, IDCC non identifié ».

**Points de vigilance** — ce qui fait basculer la réponse, ce qui est contentieux.

**Prochaines étapes** — échéancier daté si une procédure est en cours.

**Sources consultées** — liste des URL avec date de consultation.
```

Adapter la longueur à la question : une question simple mérite une réponse courte et sourcée, pas un mémoire. Les tableaux sont bienvenus pour les échéanciers et les comparaisons de scénarios de rupture.

Terminer les réponses à enjeu élevé (contentieux ouvert, salarié protégé, licenciement économique collectif, montants importants) par une phrase rappelant que ce n'est pas une consultation juridique et qu'un avocat en droit social ou l'inspection du travail doit valider.

## Spécialité — fin de contrat de travail

C'est le cœur du skill. **Lire `references/fin-de-contrat.md` dès qu'une rupture est évoquée**, quel que soit son mode. Ce fichier contient, pour chaque voie de sortie : conditions, procédure pas à pas, délais à vérifier, articles applicables, motifs d'annulation les plus fréquents.

Puis, selon le besoin :
- `references/indemnites-et-solde.md` — indemnité légale et conventionnelle, préavis, congés payés, régime social et fiscal, documents de fin de contrat, DSN et France Travail.
- `references/chomage.md` — droits à l'assurance chômage après la rupture : accès à l'ARE selon le mode de rupture, durées d'indemnisation, différés, CSP, portabilité.
- `references/cas-sensibles.md` — salarié protégé, inaptitude, maternité/parentalité, accident du travail, arrêt maladie, discrimination, harcèlement, transaction, licenciement économique et PSE, seniors.

### L'après-rupture fait partie de la réponse

Une question sur une fin de contrat n'est traitée qu'à moitié si elle s'arrête au solde de tout compte. **Dès qu'une rupture est envisagée ou subie, aborder aussi les droits au chômage** — même si l'utilisateur ne le demande pas : c'est souvent le paramètre qui détermine son choix.

Chaîner systématiquement : mode de rupture → accès à l'ARE → durée d'indemnisation → différés liés aux congés payés et aux indemnités supra-légales → date effective du premier versement. Une indemnité supra-légale plus élevée retarde le début de l'indemnisation : le dire avant que la personne signe, pas après.

### Réflexe systématique en fin de contrat

Avant de répondre sur une rupture, vérifier ces huit points — ils changent la réponse et sont oubliés une fois sur deux :

1. **Statut protégé** du salarié (mandat CSE, syndical, conseiller prud'homme, ancien élu dans la période de protection) → autorisation de l'inspection du travail obligatoire, procédure entièrement différente.
2. **État de santé et situation** : arrêt maladie, inaptitude, AT/MP, grossesse, congé maternité/paternité/parental → protections spécifiques.
3. **Ancienneté exacte** au dernier jour du contrat, préavis inclus (elle conditionne indemnité et préavis).
4. **IDCC** et dispositions conventionnelles plus favorables.
5. **Effectif** de l'entreprise (seuils : représentation du personnel, procédure économique, barème d'indemnités prud'homales).
6. **Antériorité disciplinaire** et respect du délai de prescription des faits fautifs.
7. **Clauses du contrat** : non-concurrence (contrepartie financière, levée dans les délais), dédit-formation, préavis contractuel, clause de mobilité.
8. **Date effective de fin de contrat et âge du salarié** : ce sont eux, et non la date de signature, qui déterminent le régime d'assurance chômage applicable et la durée d'indemnisation.

## Ce que ce skill ne fait pas

- Il ne remplace pas un avocat, un juriste en droit social ou l'inspection du travail.
- Il ne rédige pas de motif de licenciement à la place de l'employeur : il aide à formaliser des faits que l'employeur fournit, matériellement vérifiables et datés.
- Il ne produit pas de stratégie destinée à priver un salarié d'un droit d'ordre public.
- Il ne traite pas le droit de la fonction publique (statut, pas contrat de travail), ni le droit du travail d'autres pays. Signaler la limite et rediriger.
- Il ne prédit pas l'issue d'un contentieux : il donne des ordres de grandeur issus des textes (barème de l'article L1235-3) et des risques identifiés.

## Rédaction de documents

Pour les courriers (convocation, notification, rupture de période d'essai, réponse à une demande), partir des **modèles officiels** de code.travail.gouv.fr plutôt que d'improviser, puis les adapter. Ils sont listés dans `references/sources-officielles.md`.

Toujours faire apparaître dans le document produit les mentions dont l'absence est sanctionnée (assistance possible du salarié, délais, motifs précis et matériellement vérifiables), et signaler à l'utilisateur les champs qu'il doit compléter ou faire relire.
