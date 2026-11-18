<p align="center">
  <img src="docs/logo.svg" width="200" alt="Miza logo" />
</p>
<h1 align="center">Miza — ميزة</h1>
<p align="center">
  <a href="https://www.gnu.org/licenses/agpl-3.0"><img src="https://img.shields.io/badge/License-AGPL--3.0-blue.svg" alt="License: AGPL-3.0" /></a>
  <br />
  <strong>By Amen Allah Ben Abdrabah</strong> · Étudiant ingénieur à ENICarthage
  <br />
  <a href="https://github.com/amenallah00">GitHub</a>
</p>

<h3 align="center">ميزتك المالية — L'avantage financier qui reste entre vos mains.</h3>

<p align="center">
Les applications de finance veulent vos données. Miza, non. Nous croyons que la finance personnelle doit rester <em>personnelle</em>. Aucune société ne devrait s'interposer entre vous et vos données financières. Miza est un gestionnaire de finances open-source qui tourne sur votre propre infrastructure — conçu en Tunisie, pensé pour le monde arabe et francophone, avec un support natif du <strong>Dinar Tunisien (TND)</strong>.
</p>

## Démarrage rapide

**Linux & macOS** (utilise Docker ou Podman) :

```bash
curl -fsSL https://github.com/amenallah00/miza/install.sh | bash
```

**Windows :** Installer [Docker Desktop](https://www.docker.com/products/docker-desktop/), puis :

```bash
git clone https://github.com/amenallah00/miza.git && cd miza
docker compose up --build
```

Ouvrir [http://localhost:3000](http://localhost:3000) et créer un compte. C'est tout.

<p align="center">
  <img src="C:\Users\MSI\Pictures\Screenshots/testcap.PNG" width="800" alt="Miza dashboard" />
</p>

## Fonctionnalités

- Gestion multi-comptes avec soldes courants
- Gestion des transactions avec recherche, filtres et export CSV
- Import de fichiers (OFX, QIF, CAMT, CSV)
- Moteur de règles d'auto-catégorisation
- Transactions récurrentes, budgets et suivi de crédits/financements
- Objectifs et cibles d'épargne avec suivi de progression
- Gestion d'actifs avec valorisation et règles de croissance
- Rapports : Patrimoine net et Revenus vs Dépenses avec sparklines par catégorie
- **Support multi-devises avec conversion automatique — TND (دينار) en devise principale**
- Multi-utilisateurs avec espaces de travail, rôles et panel admin
- Passkeys, authentification à deux facteurs (TOTP) et SSO OIDC
- Synchronisation bancaire via providers (extensible)
- Agents IA (optionnel) : chat LLM auto-hébergé avec accès à vos données

### Dates de reporting et soldes bancaires

Les transactions synchronisées peuvent avoir une date de reporting modifiée sans changer la date de comptabilisation de la banque. Effacer la substitution restaure l'attribution automatique ; les syncs bancaires ultérieurs préservent la substitution.

Les périodes de reporting et les dates de liste de transactions suivent la substitution. Les soldes courants des comptes et les mouvements de flux de trésorerie suivent toujours la date bancaire (ou la date effective en mode comptabilité d'engagement).

## Capacités optionnelles

Tout ce qui va au-delà du noyau est désactivé par défaut, ne nécessite qu'un seul flag d'environnement et ne coûte rien jusqu'à activation :

- **Synchronisation bancaire** : Pluggy pour les banques brésiliennes, Enable Banking pour ~2500 banques européennes PSD2, et SimpleFIN pour les banques US et internationales.
- **Connexion & sécurité** : passkeys (Touch ID, Face ID, clés de sécurité), TOTP deux facteurs, et SSO OIDC avec liaison de compte.
- **Taux de change** : une clé [Open Exchange Rates](https://openexchangerates.org/) gratuite active la conversion automatique de devises ; sans elle, les montants inter-devises se replient sur 1:1 avec un avertissement visuel.
- **Fuseau horaire** : les soldes, budgets et dates d'échéance se réinitialisent à minuit dans le fuseau horaire de votre application.
- **Plugins** : installez des plugins communautaires dans un espace de travail depuis le catalogue de plugins.
- **Agents IA** : assistants auto-hébergés sur vos données, multi-fournisseurs, avec utilisation d'outils et une base de connaissances par agent.

## Stockage des pièces jointes

Les pièces jointes et les logos de factures utilisent le disque local par défaut. Définissez `STORAGE_PROVIDER=s3` pour les stocker dans un bucket Amazon S3 ou compatible S3 privé.

## Développement assisté par IA

Des parties de ce code ont été construites avec l'aide de l'IA. Tout le code est revu par un humain et aucune donnée ne quitte votre environnement.

## À propos de l'auteur

**Amen Allah Ben Abdrabah**
- 🎓 Étudiant ingénieur à **ENICarthage**, spécialisé en IA générative appliquée
- 🧠 Pipelines RAG / GraphRAG, agents autonomes basés sur LLM et matching sémantique
- 🩻 Segmentation de scanners CT abdominaux en 3D avec nnU-Net v2 (PyTorch, CUDA 12.4 — inférence ≈ 1 s)
- 🤖 Agent DevOps qui relit les pull requests : descriptions, labels, reviewers suggérés, synthèse CI — déployé sur Vercel + Railway
- 🌱 Approfondit actuellement l'orchestration multi-agents, les graphes de connaissances (Neo4j) et l'évaluation de RAG
- 💬 Compétences : Python, LangChain, FastAPI, PyTorch, RAG

## Contribuer

Voir [CONTRIBUTING.md](CONTRIBUTING.md) pour la configuration et les directives.

## Licence

Ce projet est sous licence [GNU Affero General Public License v3.0](LICENSE).

Cela signifie que vous pouvez librement utiliser, modifier et distribuer ce logiciel, mais toute modification — y compris lorsqu'elle est utilisée comme service réseau (SaaS) — doit également être publiée sous AGPL-3.0.

Basé sur le projet original [Securo](https://github.com/securo-finance/securo) © Tassio Noronha, sous AGPL-3.0.
Modifications et adaptation tunisienne © 2026 Amen Allah Ben Abdrabah.
