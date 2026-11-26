# droit-du-travail

Skill Claude pour le droit du travail français, inspiré de [paperasse](https://github.com/romainsimon/paperasse).

Il répond à partir des sources officielles à jour (Légifrance, code.travail.gouv.fr, service-public.fr, BOSS, Unédic, France Travail) plutôt que de mémoire, avec une spécialité sur les fins de contrat et les droits au chômage qui en découlent.

## Contenu

| Fichier | Rôle |
|---|---|
| `SKILL.md` | Instructions principales du skill |
| `profil.example.json` | Modèle de profil (statut, entreprise, IDCC, contrat…) à copier en `profil.json` |
| `references/` | Fiches : fin de contrat, chômage, indemnités et solde, cas sensibles, onboarding, sources officielles |
| `evals/evals.json` | Cas de test |

## Installation

**Claude Code** — lier le dossier dans les skills utilisateur :

```sh
ln -s ~/Projets/droit-du-travail ~/.claude/skills/droit-du-travail
```

**claude.ai** — zipper le dossier et l'importer dans *Settings → Capabilities → Skills*.

## Maintenance

Mettre à jour `metadata.last_updated` dans `SKILL.md` à chaque révision des fiches. Le skill signale lui-même ses références comme potentiellement périmées au-delà de six mois.
