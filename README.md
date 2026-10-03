# portfolio-tracker-api 
# Portfolio Tracker API

Une API REST minimale et performante développée en C# avec .NET 8 (Minimal API) pour gérer un portefeuille d'actifs financiers. Ce service backend autonome applique les principes modernes du développement web : opérations asynchrones, injection de dépendances, validation des entrées et persistance des données en mémoire via Entity Framework Core InMemory.

## Fonctionnalités
- Gestion complète (CRUD) des positions d'actifs : ajout, consultation unitaire, inventaire global, mise à jour et suppression (liquidation).
- Calcul automatique de la valeur totale de chaque ligne d'actif en fonction de la quantité et du prix d'achat unitaire.
- Documentation et test interactif des endpoints via Swagger / OpenAPI intégré.
- Validation des requêtes HTTP et renvoi de codes de statut standardisés (200 OK, 201 Created, 400 Bad Request, 404 Not Found, 204 No Content).

## Technologies utilisées
- **C# / .NET 8** (ASP.NET Core Minimal APIs)
- **Entity Framework Core InMemory** (persistance des données)
- **Swashbuckle / OpenAPI** (documentation interactive)

## Démarrage rapide

### Prérequis
- [.NET 8 SDK](https://dotnet.microsoft.com/download) installé sur votre machine.

### Installation et exécution
1. Cloner le dépôt :
   git clone https://github.com/votre-nom-utilisateur/portfolio-tracker-api.git
   cd portfolio-tracker-api

2. Restaurer les dépendances et lancer l'application :
   dotnet run

3. Accéder à la documentation interactive Swagger :
   Ouvrez votre navigateur à l'adresse suivante : `https://localhost:xxxx/swagger` (le port exact est indiqué dans la console au démarrage).

## Endpoints principaux
- `GET /api/portfolio` : Récupère la liste de tous les actifs du portefeuille.
- `GET /api/portfolio/{id}` : Récupère les détails d'un actif par son identifiant.
- `POST /api/portfolio` : Enregistre un nouvel actif (symbole, quantité, prix d'achat).
- `PUT /api/portfolio/{id}` : Met à jour la quantité ou le prix d'achat d'un actif.
- `DELETE /api/portfolio/{id}` : Supprime un actif du portefeuille.
