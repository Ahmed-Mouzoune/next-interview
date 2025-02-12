# Test Technique Next.js

## Configuration initiale

1. Créez un nouveau projet Next.js avec TypeScript :

```bash
npx create-next-app@latest next-interview --typescript --tailwind --eslint
cd mon-test-technique
```

2. Installez les dépendances shadcn/ui nécessaires :

```bash
npx shadcn-ui@latest init
```

## Tâches à réaliser

### 1. Affichage des produits avec pagination

Créez un composant `ProductCard` qui affiche les informations d'un produit, et utiliser pour afficher tout les produits du fichier products.ts, et implémentez la pagination. Vous devrez utiliser les composants shadcn/ui suivants :

- [Card](https://ui.shadcn.com/docs/components/card)
- [Badge](https://ui.shadcn.com/docs/components/badge)
- [Button](https://ui.shadcn.com/docs/components/button)

Installation des composants :

```bash
npx shadcn-ui@latest add card
npx shadcn-ui@latest add badge
npx shadcn-ui@latest add button
```

Créez un hook personnalisé `usePagination` qui :

- Accepte un tableau de données et la taille de la page
- Retourne les données paginées et les fonctions de navigation
- Gère le changement de page et le calcul des pages totales

### 2. Intégration API

1. Créez un hook `useProducts` qui :

   - Utilise initialement les données locales du fichier `products.ts`
   - Prépare la structure pour basculer vers un appel API
   - Gère les états de chargement et d'erreur

2. Remplacez les données locales par un appel API :
   - Endpoint à utiliser : `https://fakestoreapi.com/products`
   - Adaptez les données reçues au format de votre interface Product
   - Gérez les états de chargement et d'erreur dans l'UI

### 3. Bonus - Mode Sombre (5 minutes)

Implémentez un toggle pour basculer entre le mode clair et sombre :

1. Installez next-themes :

```bash
npm install next-themes
```

2. Suivez la documentation de shadcn/ui pour l'implémentation du mode sombre.

## Aperçu du résultat attendu

Vous pouvez consulter la version finale du test sur [URL_DU_DEPLOIEMENT] pour avoir un aperçu du résultat attendu.
