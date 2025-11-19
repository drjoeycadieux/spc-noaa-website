## 🗺️ GeoAlerts - Carte d'Alertes Géomatiques et Météorologiques

---

## 🎯 Aperçu du Projet

Ce projet est une application web simple utilisant **Leaflet.js** pour visualiser des données géospatiales provenant de diverses sources d'alertes météorologiques et de pannes d'électricité en Amérique du Nord et au Québec.

Il combine des couches de données en direct ou semi-live pour fournir une vue d'ensemble rapide des conditions.

### Sources de Données Intégrées

- **⚡ Hydro-Québec Outages (Pannes) :** Affiche les zones de pannes d'électricité actives au Québec (utilisant un proxy CORS pour l'accès).
- **🌩️ SPC NOAA (Storm Prediction Center) :** Affiche les risques de temps violent (Marginal, Slight, Enhanced, Moderate, High) aux États-Unis, avec une fonction d'animation d'opacité.
- **📡 NEXRAD Radar :** Superposition de tuiles radar en temps quasi-réel.
- **🚨 MSC CAP Alert (Modèle) :** Affiche un exemple d'alerte CAP (Common Alerting Protocol) pour démontrer l'intégration des alertes météorologiques canadiennes.
- **🏛️ IGO Québec (MSP) :** Couche de base et événements historiques géospatiaux du gouvernement du Québec.

---

## 🚀 Comment Exécuter le Projet

Ce projet est un simple fichier HTML. Vous n'avez besoin d'aucun environnement de développement ou serveur complexe.

### 1. Sauvegarder les Fichiers

1.  Enregistrez le code HTML/CSS/JavaScript complet que nous avons élaboré dans un seul fichier nommé, par exemple, `index.html`.

### 2. Ouvrir dans le Navigateur

1.  Ouvrez ce fichier `index.html` directement dans votre navigateur web (Chrome, Firefox, Edge, etc.) en double-cliquant dessus.

L'application chargera la carte et tentera de récupérer les données des différentes sources.

---

## ⚙️ Détails Techniques Clés

Le code utilise principalement des technologies front-end standard :

- **HTML5/CSS3 :** Structure et style.
- **JavaScript (ES6+) :** Logique de chargement des données.
- **Leaflet.js :** Bibliothèque JavaScript légère pour les cartes interactives.

### ⚠️ Contournement CORS pour Hydro-Québec

Pour accéder aux données de pannes d'Hydro-Québec à partir d'un domaine externe, le code utilise un service de **proxy CORS** public (`https://corsproxy.io/`).

```javascript
// La fonction loadHydroQuebecOutages utilise un proxy pour contourner la politique CORS:
const hydroQuebecApiUrl =
  "[https://corsproxy.io/?https://pannes.hydroquebec.com/pannes/donnees/v3_0/bisversion.json](https://corsproxy.io/?https://pannes.hydroquebec.com/pannes/donnees/v3_0/bisversion.json)";
```
