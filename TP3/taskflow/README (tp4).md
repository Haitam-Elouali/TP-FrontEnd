Q1 : Combien de lignes de CSS avez-vous écrit pour le Header MUI ? Comparez avec 
votre Header.module.css

0 lignes, Tout le style est dans sx={{}} contrairement a Header.module.css (fichier css externe utiliser).

Q2 : Comparez le code du Header MUI vs Bootstrap. Lequel est plus lisible ? Plus court ? 

Le code Header MUI est plus lisible mais long dans l'ecriture du logic, contrairement a Bootstrap qui melange jsx avec les class (moins lisible) mais plus court dans l'ecriture du logic. 

Q3 : Le Login MUI utilise sx={{}} pour le style. Le Login Bootstrap utilise des classes CSS 
(className). Quel système préférez-vous ? Pourquoi ?

Je préfère MUI car le style est directement intégré dans le composant, ce qui facilite la maintenance et la cohérence du design.

Tableau comparatif

| Critère                   | Material UI    | React-Bootstrap   |
| ------------------------- | -------------- | ----------------- |
| Installation              | Moyenne        | Facile            |
| Composants utilisés       | Beaucoup       | Moins             |
| Lignes de CSS             | 0              | Peu               |
| Système de style          | sx (JS)        | className (CSS)   |
| Personnalisation couleurs | Très facile    |  Limitée          |
| Responsive                | Très bon       | Bon               |
| Lisibilité du code        | Meilleure      | Moyenne           |
| Documentation             | Très riche     | Bonne             |
| Préférence                | De plus        | De moins          |

Q4 : Si vous deviez choisir UNE seule library pour TaskFlow en production, laquelle et 
pourquoi ?

Je choisirais Material UI pour la production car il offre une meilleure intégration avec React, un système de style puissant et une meilleure maintenabilité du code.

Architecture Base de Données

React (localhost:5173) avec HTTP (GET, POST, PUT, DELETE) -> Axios -> json-server (localhost:4000) -> db.json

a) Firebase

React → Firebase SDK → Firebase Database

b) Express + MongoDB

React → Axios → Express API → MongoDB

Q5 : Pourquoi React ne peut-il PAS se connecter directement à MySQL ?

Pour des raison de securite, le client ne peut pas directement modifier la base de données.

Q6 : json-server est parfait pour notre TP. Donnez 3 raisons pour lesquelles on ne 
l’utiliserait PAS en production.

Pas sécurisé, pas performant, pas de logique métier.

Q7 : Firebase permet à React de se connecter directement (pas de backend Express). 
Comment est-ce possible alors que MySQL ne le permet pas ?

Puisque Firebase fournit une API HTTP, un SDK et une haute securité qui sont tous integrées. Alors que MySQL n'as pas d’API web native.

Q8 : Votre TaskFlow utilise json-server. Un client vous demande de passer en production 
avec de vrais utilisateurs. Quelles étapes sont nécessaires ? 

Remplacer json-server -> Ajouter authentification (JWT) -> Base de données réelle -> Déploiement -> Sécurité (HTTPS) -> Tests

Q9 : MUI et Bootstrap sont des libraries externes. Quel est le risque d’en dépendre ? (indice : pensez à la taille du bundle et aux mises à jour)

- Bundle lourd
- Mises à jour cassantes
- Dépendance externe

Q10 : Vous devez créer une app de chat en temps réel. json-server, Firebase ou Backend 
custom ? Justifiez.

Je choisirais Firebase pour sa gestion native du temps réel. Pour une application plus complexe, un backend custom avec WebSocket serait préférable.