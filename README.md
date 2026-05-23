# INPAF - Site Web

Dépôt du projet de site web de l'INPAF.

---

## Stack technique

| Couche | Technologie |
|---|---|
| Frontend | React |
| Backend | Django |
| Base de données | MySQL |
| Hébergement Web | Infomaniak |

---

## Architecture du dépôt

```
inpaf/
├── frontend/    # Applications React (site web, administration, mobile)
├── backend/     # Application Django
├── docs/        # Documentation technique et fonctionnelle (un dossier par fonctionnalité)
├── deploy/      # Scripts, infra et configuration de déploiement
└── README.md
```

---

## Branches

| Branche | Rôle |
|---|---|
| `master` | Production — miroir exact de l'environnement de prod |
| `recette` | Validation fonctionnelle et tests d'intégration avant mise en prod |
| `développement` | Intégration du travail de tous les développeurs |

**Workflow :** chaque développeur crée sa propre branche de fonctionnalité depuis `développement`, puis la merge sur `développement` une fois terminée. Les montées en prod passent par `recette` avant `master`.

---

## Mise en place locale

### Prérequis

- Node.js >= 18
- Python >= 3.10
- MySQL >= 8

### Frontend

```bash
cd apps/frontends/nom1
npm install
npm run dev
```

### Backend

```bash
cd apps/backend
python -m venv venv
source venv/bin/activate      # Windows : venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env          # Configurer les variables d'environnement
python manage.py migrate
python manage.py runserver
```

---

## Lancement

```bash
# Frontend (site web)
cd apps/frontends/nom1 && npm run dev

# Backend
cd apps/backend && python manage.py runserver
```

---

## Conventions et normes de développement

- Les messages de commit sont rédigés en français, au présent et de façon concise.
- Toute nouvelle fonctionnalité doit avoir son dossier de documentation dans `docs/`.
- Le code est relu (code review) avant tout merge sur `développement`.
- Les variables d'environnement sensibles ne sont jamais commitées — utiliser `.env` (ignoré par git).
- Les branches de fonctionnalité suivent la convention : `feature/nom-de-la-fonctionnalite`.

---

## Membres de l'équipe

| Email |
|---|
| abdallahrohad@gmail.com |
| csbakayoko@gmail.com |
| ziontech1998@gmail.com |
| kessegabriel@gmail.com |
| fabrice.fkouame@gmail.com |
| bakary.kouame@inphb.ci |
| trohkopeemmanuel@gmail.com |

---

## Contact en cas de problème

En cas de blocage ou d'incident, contacter en priorité : **ziontech1998@gmail.com**
