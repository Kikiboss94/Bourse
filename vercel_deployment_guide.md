# Guide de déploiement sur Vercel

Ce guide vous explique comment déployer votre application d'analyse boursière en temps réel sur Vercel pour bénéficier de toutes les fonctionnalités API.

## Prérequis

1. Un compte [Vercel](https://vercel.com/signup) (gratuit pour les projets personnels)
2. Un compte GitHub, GitLab ou Bitbucket pour héberger votre code

## Étapes de déploiement

### 1. Préparation du dépôt Git

1. Créez un nouveau dépôt sur GitHub, GitLab ou Bitbucket
2. Clonez le dépôt sur votre machine locale
3. Copiez tous les fichiers du projet dans le dépôt
4. Commitez et poussez les changements vers votre dépôt

### 2. Configuration de Vercel

1. Connectez-vous à votre compte Vercel
2. Cliquez sur "Add New..." puis "Project"
3. Connectez votre compte GitHub, GitLab ou Bitbucket si ce n'est pas déjà fait
4. Sélectionnez le dépôt contenant votre projet d'analyse boursière
5. Dans les paramètres de configuration :
   - Framework Preset : Next.js
   - Root Directory : laissez vide si votre projet est à la racine du dépôt
   - Build Command : `next build`
   - Output Directory : `.next`
   - Install Command : `npm install`

6. Dans la section "Environment Variables", ajoutez les variables suivantes :
   - `NEXT_PUBLIC_API_URL` : `https://query1.finance.yahoo.com`

7. Cliquez sur "Deploy"

### 3. Vérification du déploiement

1. Une fois le déploiement terminé, Vercel vous fournira une URL pour accéder à votre application
2. Vérifiez que toutes les fonctionnalités fonctionnent correctement :
   - Affichage des cours boursiers
   - Mises à jour en temps réel
   - Recherche et filtrage des actions et ETFs
   - Listes de surveillance

### 4. Configuration d'un domaine personnalisé (optionnel)

1. Dans le tableau de bord Vercel, sélectionnez votre projet
2. Allez dans l'onglet "Settings" puis "Domains"
3. Ajoutez votre domaine personnalisé et suivez les instructions pour configurer les DNS

## Optimisations pour Vercel

Le code a été optimisé pour fonctionner parfaitement sur Vercel :

1. Configuration Next.js adaptée pour Vercel
2. Utilisation d'APIs publiques pour les données boursières
3. Gestion du cache côté client pour optimiser les performances
4. Interface responsive pour mobile et desktop

## Support et maintenance

Pour toute question ou problème avec le déploiement, n'hésitez pas à me contacter. Je peux vous aider à résoudre les problèmes ou à apporter des améliorations à votre application d'analyse boursière en temps réel.
