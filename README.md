[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/JA95QPrH)
# R212-2024-TP4

À partir de ce repository, réaliser les tâches suivantes :

- Créer un nouveau composant `Button.vue`
- Créer les props suivantes :
  - `variant?: 'default' | 'dark' | 'outlined'`
  - `size?: 'small' | 'medium' | 'large'`
  - `url?: string`
  - `text?: string`
  - `icon?: string | object | undefined`
- avec les valeurs par défaut suivantes :
  - `variant: 'default'`,
  - `size: 'medium'`
- Créer deux objets `variantClass` et `sizeClass` avec pour chaque clé (définies dans les props `variant` et `size`) les classes tailwind permettant la mise en forme de chaque variant.
- Pour l'icône, utiliser un composant dynamique (https://vuejs.org/guide/essentials/component-basics#dynamic-components)
- Dans `HeaderPage.vue`, remplacer les deux boutons _login_ et _sign up_ par le composant `Button.vue`
