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

### Préparer le zip (pour les imports par upload)

claude.ai et ChatGPT attendent un `.zip` dont le dossier racine contient `SKILL.md` :

```sh
git clone https://github.com/thomandre/droit-du-travail.git
zip -r droit-du-travail.zip droit-du-travail -x 'droit-du-travail/.git/*'
```

### Claude Code

```sh
git clone https://github.com/thomandre/droit-du-travail.git ~/.claude/skills/droit-du-travail
```

Le skill se charge tout seul dès qu'une question touche au droit du travail. Pour le mettre à jour : `git -C ~/.claude/skills/droit-du-travail pull`.

### Claude Desktop / claude.ai

1. Dans les réglages, section *Capabilities*, activez **Code execution and file creation**. Sans cette option, l'upload échoue.
2. Dans *Customize → Skills*, uploadez `droit-du-travail.zip`.

### ChatGPT

Sur les offres Business, Enterprise, Healthcare et Edu, ChatGPT accepte l'upload de skills si l'administrateur de l'espace de travail l'autorise ([aide OpenAI](https://help.openai.com/en/articles/20001066-skills-in-chatgpt)). Uploadez `droit-du-travail.zip`.

### Profil

Au premier usage, le skill pose quelques questions : votre statut, la taille de l'entreprise, la convention collective, le contrat. Pour ne pas répondre à chaque fois, copiez `profil.example.json` en `profil.json` dans votre dossier de travail et remplissez-le. Le fichier est ignoré par git.

## Maintenance

Mettre à jour `metadata.last_updated` dans `SKILL.md` à chaque révision des fiches. Le skill signale lui-même ses références comme potentiellement périmées au-delà de six mois.
