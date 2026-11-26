# Indemnités, préavis, solde de tout compte, documents de fin de contrat

Ce fichier donne la **méthode**. Les taux, plafonds, tranches et barèmes se récupèrent à chaque fois sur les sources officielles — ils changent au moins une fois par an (plafond annuel de la sécurité sociale, SMIC, barèmes, avenants de branche).

## 1. Méthode de calcul d'une indemnité de rupture

Toujours produire **trois lignes**, dans cet ordre :

1. **Calcul légal** — formule du Code du travail.
2. **Calcul conventionnel** — formule de la CCN (IDCC), qui prévoit souvent une base ou un taux plus favorables, parfois avec majoration selon l'âge ou le statut cadre.
3. **Montant retenu** = le plus favorable au salarié, **avantage par avantage**, sans panachage des deux formules.

Puis mentionner ce qui s'ajoute éventuellement : indemnité supra-légale négociée, indemnité compensatrice de préavis, indemnité compensatrice de congés payés, contrepartie de non-concurrence, primes au prorata, épargne salariale.

### Paramètres à réunir avant tout calcul

- Date d'entrée, date de notification, date de fin de contrat **préavis inclus** (l'ancienneté s'apprécie au terme du préavis, exécuté ou non).
- Ancienneté reprise (transfert L1224-1, groupe, clause contractuelle).
- Salaire de référence : la formule légale retient la moyenne la plus favorable entre plusieurs périodes de référence — vérifier la définition en vigueur et le traitement des primes annuelles, du variable, des périodes d'absence non rémunérées, des périodes à temps partiel.
- Alternance temps plein / temps partiel au cours de la carrière : proratisation par périodes. Le simulateur officiel ne gère pas ce cas — le signaler.
- Statut, classification, âge quand la CCN en tient compte.

### Cas où l'indemnité de licenciement n'est pas due

Faute grave, faute lourde, et situations propres à certains modes de rupture (démission, fin de CDD). Attention : même en faute grave, **l'indemnité compensatrice de congés payés reste due**.

### Outils officiels

Simulateurs de code.travail.gouv.fr (`indemnite-licenciement`, `indemnite-rupture-conventionnelle`, `indemnite-precarite`). Les utiliser comme contrôle et proposer le lien à l'utilisateur. Ils intègrent une cinquantaine de conventions collectives ; hors de cette liste, ils ne donnent que le plancher légal — le préciser.

## 2. Préavis

- **Licenciement** : durée légale minimale (L1234-1) selon l'ancienneté, sauf disposition conventionnelle, contractuelle ou usage plus favorable. Pas de préavis en faute grave ou lourde.
- **Démission** : pas de durée légale générale — c'est la CCN, le contrat ou l'usage qui s'appliquent.
- **Retraite** : préavis aligné sur celui du licenciement, sauf disposition plus favorable.
- **Dispense de préavis** : à l'initiative de l'employeur, le salaire reste dû (indemnité compensatrice, avec maintien des avantages) ; à la demande du salarié acceptée par l'employeur, rien n'est dû.
- **Point de départ** : notification (date de première présentation de la lettre recommandée, à vérifier selon le mode de rupture).
- **Incidents pendant le préavis** : arrêt maladie (ne le prolonge pas en principe, sauf accident du travail ou disposition conventionnelle), congés payés, dispense partielle. Vérifier la fiche du Code du travail numérique **dans la version de la CCN concernée**.
- **Heures de recherche d'emploi** : prévues par de nombreuses conventions collectives et usages ; simulateur officiel `heures-recherche-emploi`.

## 3. Solde de tout compte

Composition à passer en revue systématiquement — c'est la check-list qui évite les rappels :

- salaire du mois de sortie, au prorata ;
- indemnité compensatrice de préavis le cas échéant ;
- indemnité compensatrice de congés payés (congés acquis non pris, y compris ceux acquis pendant certains arrêts de travail — le régime a évolué, vérifier) ;
- RTT et jours de repos non pris, compte épargne-temps ;
- indemnité de licenciement / rupture conventionnelle / départ à la retraite / fin de contrat ;
- primes et variables au prorata (13e mois, objectifs, ancienneté), selon les conditions d'ouverture du droit ;
- contrepartie financière de non-concurrence — vérifier si l'employeur a levé la clause **dans le délai prévu** ; à défaut, elle est due ;
- remboursement de frais professionnels, avantages en nature à régulariser ;
- retenues éventuelles : trop-perçu, matériel non restitué (dans les limites légales, aucune compensation automatique sur salaire hors cas prévus), dédit-formation si la clause est valable ;
- intéressement, participation, PEE/PERCO : information sur le devenir des avoirs et les cas de déblocage.

**Reçu pour solde de tout compte** (L1234-20) : établi en double exemplaire, il fait l'objet d'un délai de dénonciation ; passé ce délai, il devient libératoire **pour les seules sommes qui y sont mentionnées**. D'où l'importance d'un détail poste par poste. Modèle officiel disponible sur code.travail.gouv.fr.

## 4. Documents de fin de contrat

À remettre au terme du contrat, quel que soit le motif de rupture :

- **Certificat de travail** (L1234-19) — mentions limitativement prévues.
- **Reçu pour solde de tout compte** (L1234-20).
- **Attestation destinée à France Travail** (R1234-9) — transmise par la DSN ; vérifier les modalités en vigueur sur `francetravail.fr`.
- **État récapitulatif de l'épargne salariale** le cas échéant.
- **Information sur la portabilité** de la complémentaire santé et prévoyance (maintien des garanties, durée et conditions à vérifier).
- Dernier **bulletin de paie**.

Ces documents sont **quérables ou portables** selon leur nature : leur non-remise ou leur remise tardive engage la responsabilité de l'employeur et peut donner lieu à un référé prud'homal. Modèle de lettre de réclamation disponible sur code.travail.gouv.fr.

## 5. Régime social et fiscal des indemnités de rupture

Ne jamais annoncer un montant net sans avoir vérifié le régime en vigueur. Points à contrôler :

- exonération de **cotisations sociales** dans certaines limites indexées sur le **plafond annuel de la sécurité sociale** — barème sur `boss.gouv.fr`, rubrique indemnités de rupture ;
- assujettissement à la **CSG-CRDS** selon des règles distinctes de celles des cotisations ;
- **contribution patronale spécifique** applicable à certaines indemnités de rupture conventionnelle ou de mise à la retraite — taux à vérifier, il a changé ;
- **imposition sur le revenu** : exonération partielle selon la nature de l'indemnité, et régime différent lorsque le salarié est en droit de liquider une retraite à taux plein — voir `impots.gouv.fr` ;
- **indemnité compensatrice de préavis et de congés payés** : traitées comme du salaire, donc soumises à cotisations et impôt ;
- **indemnité transactionnelle** : régime dépendant de sa nature (indemnitaire ou salariale) et de sa qualification dans le protocole.

Quand un utilisateur demande « combien il touchera », répondre en **brut**, décomposé, puis indiquer que le net dépend du régime ci-dessus et proposer de le vérifier poste par poste.

## 6. Assurance chômage

Traité en détail dans `chomage.md` — s'y reporter systématiquement dès qu'une rupture est en jeu. Retenir ici seulement que l'indemnité supra-légale **retarde** le début de l'indemnisation via le différé spécifique, et que la durée d'indemnisation dépend du mode de rupture, de l'âge et de la date de fin de contrat.

## 7. Transaction

Postérieure à la rupture définitive (jamais concomitante), écrite, avec **concessions réciproques** réelles. Elle éteint le litige dans les limites de son objet. Une transaction signée avant la notification de la rupture, ou sans concession réelle, est nulle.

Rédiger avec un avocat : la portée de la clause de renonciation détermine ce que le salarié abandonne. Signaler à un salarié qui la reçoit qu'il peut la faire relire avant de signer, et qu'il n'y a pas d'urgence à signer sur le champ.
