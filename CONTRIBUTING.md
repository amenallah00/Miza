# Contribuer à Miza (ميزة)

Merci de l'intérêt que vous portez à Miza ! Ce guide vous aidera à démarrer.

## Pour commencer

1. Forkez le dépôt
2. Clonez votre fork : `git clone https://github.com/amenallah00/miza.git`
3. Démarrez la stack : `docker compose up --build`
4. Ouvrir [http://localhost:3000](http://localhost:3000)

## Par où commencer

Nouveau ici ? La contribution la plus facile est petite et auto-contenue :

- Parcourez les [issues ouvertes](https://github.com/amenallah00/miza/issues), en particulier celles étiquetées `good first issue` ou `help wanted`.
- Les petites corrections de bugs, les améliorations de documentation et les mises à jour de traduction sont toujours les bienvenues.
- Commentez une issue pour indiquer aux autres que vous la prenez en charge.

## Avant les grands changements ou les changements de cœur

Pour tout ce qui est plus grand — une nouvelle fonctionnalité, un refactoring, ou un changement d'un mécanisme de base — nous aimerions en discuter **avant** que vous écriviez le code.

Bonnes façons d'aligner d'abord :

- Ouvrez une [demande de fonctionnalité](.github/ISSUE_TEMPLATE/feature_request.md).
- Commentez l'issue correspondante si elle existe déjà.

## Décisions d'architecture

Les règles que le code respecte, et où chaque fonctionnalité vit, sont dans [`AGENTS.md`](AGENTS.md). Les raisons derrière elles sont dans [`docs/adr/`](docs/adr/README.md).

## Utiliser l'IA

Utilisez-la. Des parties de ce code ont été écrites avec de l'IA. Ce n'est pas une politique contre les outils.

C'est une politique de propriété. **Nous ne revoyons pas l'IA, nous vous revoyons.** Quand une PR arrive, les questions sont les mêmes qu'elles ont toujours été : cette personne comprend-elle ce qu'elle propose, peut-elle expliquer pourquoi c'est construit ainsi, et sera-t-elle encore là si ça casse.

Donc, quelle que soit votre utilisation, avant d'ouvrir la PR :

- **Vous êtes propriétaire de l'approche, pas seulement de la sortie.**
- **Vous êtes la porte qualité.**
- **Ça s'intègre là où le produit va.**
- **Vous l'avez testé.** Pas "les tests devraient passer" — vous les avez lancés.

## Tests

Lancez lint, vérification de types et les tests que vous avez touchés avant de déclarer le travail terminé ; CI lance le reste.

```bash
# Backend
cd backend && uv sync --all-extras
uv run pytest
uv run ruff check . && uv run ty check .

# Frontend
cd frontend && npm run lint && npm run build && npm test
```

## Commits conventionnels

Format : `feat:`, `fix:`, `docs:`, `refactor:` — une fonctionnalité ou correction par pull request, tests backend pour tout nouveau comportement.

## À propos du mainteneur

**Amen Allah Ben Abdrabah** · Étudiant ingénieur à ENICarthage, Tunisie
Spécialisé en IA générative : RAG, agents LLM, matching sémantique.
