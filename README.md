# Sourcing de leads — INSEE Sirene

Outil web autonome (un seul fichier, `index.html`) pour trouver des entreprises cibles dans le répertoire Sirene de l'INSEE, à partir de critères NAF, géographie et effectif, puis les exporter en CSV.

Aucun serveur, aucune dépendance externe : le navigateur interroge directement `api.insee.fr`.

## Utilisation

1. Ouvrez la page (GitHub Pages ou en local) et collez votre clé API Sirene (à créer sur [portail-api.insee.fr](https://portail-api.insee.fr), application abonnée à l'API Sirene).
2. Renseignez la cible : codes NAF (`62.01Z`, `6201Z` ou préfixe `62`), départements et/ou région, tranches d'effectif.
3. Cliquez sur **Trouver les leads**, filtrez/triez le tableau, puis **Exporter en CSV** (format Excel FR, séparateur `;`).

## Confidentialité

La clé API n'est jamais stockée dans ce dépôt. Elle reste dans le navigateur de l'utilisateur (option de mémorisation limitée à l'onglet) et n'est envoyée qu'à l'INSEE, via l'en-tête `X-INSEE-Api-Key-Integration`.

## Lancer en local

```bash
python -m http.server
```

puis ouvrir <http://localhost:8000/>.

## Publier sur GitHub Pages

Settings → Pages → Source : *Deploy from a branch*, branche `main`, dossier `/ (root)`.

## Source des données

INSEE, répertoire Sirene — données publiques sous Licence Ouverte. Attention au RGPD pour les entrepreneurs individuels (personnes physiques).
