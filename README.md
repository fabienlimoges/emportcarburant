# Emport carburant — Navigation 3 étapes (exercice PPL)

Outil d'aide à la préparation du bilan carburant pour la navigation en 3 étapes
de l'exercice PPL. L'objectif est de garantir l'emport réglementaire au départ
de la troisième étape.

**➡️ Application en ligne : https://fabienlimoges.github.io/emportcarburant/**

Sur iPad / iPhone : ouvrir l'URL dans Safari → Partager → « Sur l'écran
d'accueil » pour l'installer comme une app.

## Utilisation

Ouvrir l'URL ci-dessus, ou `emport-carburant.html` dans un navigateur
(double-clic). Aucune installation ni serveur nécessaire — le fichier peut
aussi être copié tel quel sur chaque poste de l'aéroclub.

- Champs encadrés = à remplir, le reste se calcule automatiquement.
- Forfaits fixes : roulage 5 min et intégration terrain d'arrivée 10 min par étape.
- Aléas en % de la conso, réglables étape par étape.
- Étape 3 : plan de diversion, marge CDB, réserve finale (30 min jour / 45 min nuit)
  et quantité inutilisable.

## Configurer la flotte

La flotte est codée en dur dans `emport-carburant.html`, dans le bloc
`⚙️ FLOTTE DU CLUB` en tête du `<script>` :

```javascript
const FLEET = [
  {immat:"F-GGXD", conso:25, inut:4, capa:110},
  ...
];
```

Pour chaque avion : immatriculation, consommation horaire (L/h), carburant
inutilisable (L) et capacité totale des réservoirs (L) — valeurs à reprendre
du manuel de vol.

## Contenu

- `emport-carburant.html` — l'application (fichier autonome).
- `emport_carburant_ppl.xlsx` — version tableur (Numbers / Google Sheets),
  antérieure à l'application ; l'application HTML est l'outil de référence.

⚠️ Outil d'aide à la préparation — le commandant de bord reste responsable du
bilan carburant.
