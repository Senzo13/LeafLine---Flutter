# Leafline 🌱

<div align="center" style="text-align: center;">
  <img src="background-mockup.jpg" alt="Leafline" width="80%" />
</div>

## Description 🔬

Leafline est une application utilisant l'IA et des capteurs IoT pour protéger les plantes en prévisualisant la météo. Les capteurs surveillent en temps réel l'humidité du sol, la température et l'intensité lumineuse. L'application analyse les données et les prévisions météorologiques pour avertir les utilisateurs des risques encourus par leurs plantes, tels que les maladies causées par la pluie. Des notifications et des conseils personnalisés sont fournis pour prendre des mesures préventives et préserver la santé des plantes.

## Checklist des fonctionnalités 📝

- Navigation (CustomTabBar) : ✔️
- Map : ❌
- Inscription et connexion : ❌
- Home : ❌
- Dashboard : ❌
- Settings : ❌

## Technologies 🛠

Les technologies suivantes ont été utilisées dans le développement de ce projet :

### Frontend 💻

- [Flutter](https://flutter.dev/) ![Flutter logo](https://img.shields.io/badge/-Flutter-02569B?style=flat-square&logo=flutter&logoColor=white)

## Architecture 🏛️

Leafline utilise une architecture MVVM (Model-View-ViewModel), offrant une séparation claire des préoccupations et rendant l'application plus modulaire et maintenable. Voici une brève explication de l'implémentation de cette architecture :

- **Model** : Il représente les données et la logique métier de l'application. Par exemple, pour une vue de connexion, nous aurions un modèle de connexion qui contient des informations typées pour le login.

- **View** : Il s'agit de la partie frontale de l'application. Elle est organisée en deux dossiers principaux :

  - **Tabs** : Contient les vues principales ou les onglets de l'application.
  - **Others** : Regroupe toutes les autres pages ou vues qui ne sont pas considérées comme principales.

- **ViewModel** : Il sert d'intermédiaire entre la Vue et le Modèle. Il contient la logique de la vue et met à jour la vue en utilisant `ChangeNotifier` chaque fois que le modèle est modifié. Tout comme la vue, le ViewModel est également organisé en dossiers "Tabs" et "Others".

- **Service** : Cette couche gère les interactions externes telles que les requêtes API. Par exemple, lors de la connexion d'un utilisateur, c'est le service qui envoie la demande à l'API et reçoit la réponse.

Avec cette architecture, chaque composant a une responsabilité claire, rendant le code plus propre et plus facile à tester et à déboguer.

**Suivis de développement sur Jira Atlassian**

> _https://farming4cast.atlassian.net/jira/software/projects/LEAFLINE/boards/1_

## Installation et Commandes Utiles 📟

### Prérequis

- Assurez-vous d'avoir [Flutter](https://flutter.dev/docs/get-started/install) installé sur votre machine.
- Vérifiez la version de Flutter : `flutter --version`

### Commandes

- Cloner ce dépôt : `git clone https://gitlab.com/t-esp-app-flutter/leafline-app`
- Accéder au dossier du projet : `cd leafline-app`
- Installer les dépendances : `flutter pub get`
- Lancer l'application sur un émulateur ou un appareil physique : `flutter run`
- Pour construire l'application pour une release : `flutter build apk` (pour Android) ou `flutter build ios` (pour iOS).

## Plugins 🧩

- **Dio** ![Dio logo](https://img.shields.io/badge/-Dio-5f4b8b?style=flat-square) : Version utilisée : `dio: ^5.3.2`.

- **Shared Preferences** ![Shared Preferences logo](https://img.shields.io/badge/-SharedPreferences-34b7f1?style=flat-square) : Version utilisée : `shared_preferences: ^2.2.1`

## Running Tests 🧪

Pour exécuter les tests, utilisez cette commande :

```bash
  flutter test
```
