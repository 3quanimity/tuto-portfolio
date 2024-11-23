<script setup>
import { ref } from "vue";
import ProjectSingle from "./ProjectSingle.vue";

let projects = ref([
  {
    name: "Projet N°1: Jeu du Nanogram",
    images: ["projet1.png"],
    tags: "VueJS CDN",
    description:
      "Un générateur de grilles et de puzzles de Nonogrammes, développé avec Vue 3 en utilisant le CDN pour une configuration légère et rapide.",
    tasks:
      "Conception des algorithmes de génération de grilles.;Mise en place de la logique de résolution interactive.",
    githubLink: "https://github.com/3quanimity/nonogram",
  },
  {
    name: "Projet N°2: Dashboard Vuetify",
    images: ["projet2.png"],
    tags: "VueJS;Vuetify;VueChart3",
    description:
      "Un tableau de bord interactif permettant d'explorer les revenus d'une entreprise, regroupés par pays et provenant de diverses applications et publicités. Développé avec Vue 3, utilisant les data-tables Vuetify pour une navigation fluide et des graphiques dynamiques avec VueChart3.",
    tasks:
      "Intégration des données via une API REST.;Conception et personnalisation des data-tables avec Vuetify.;Graphiques interactifs pour des analyses visuelles claires.",
    githubLink: "https://github.com/3quanimity/vuetify-dashboard",
  },
  {
    name: "Projet N°3: Site d'Actualité",
    images: ["projet3.png"],
    tags: "VueJS;NuxtJS;Bootstrap",
    description:
      "Une interface moderne pour afficher des articles d'actualité extraits d'une API, avec une mise en page stylisée grâce à Bootstrap et une redirection vers les articles correspondants.",
    tasks:
      "Connexion à une API tierce pour la récupération des données.;Création d'une mise en page responsive avec Bootstrap.;Liens dynamiques pour une navigation directe vers les articles.",
    githubLink: "https://github.com/3quanimity/vue3-nuxt-news-site",
  },
  {
    name: "Projet N°4: Application de Gestion",
    images: [
      "projet4-1.png",
      "projet4-2.png",
      "projet4-3.png",
      "projet4-4.png",
      "projet4-5.png",
      "projet4-6.png",
      "projet4-7.png",
    ],
    tags: "VueJS;NuxtJS;Vuetify;REST API",
    description:
      "Une application de gestion complète pour la création et la suppression d'utilisateurs et de projets. Elle inclut un tableau de bord interactif pour la visualisation des données et le suivi des indicateurs clés de performance (KPI), avec des fonctionnalités d'authentification et de gestion de sessions utilisateur.",
    tasks:
      "API REST pour la gestion des utilisateurs et des projets.;Tableau de bord interactif avec des composants Vuetify.;Fonctionnalités d'authentification sécurisées.",
    githubLink: "https://github.com/3quanimity/nuxt-vue-vuetify-management-app",
  },
]);
</script>

<template>
  <div id="projects">
    <h2 class="text-highlight-1 section-title">
      Projets réalisés au cours de la formation Vue 3
    </h2>
    <ProjectSingle
      v-for="(project, index) in projects"
      :key="project.name"
      :project="project"
      :reverse="index % 2 === 0 ? false : true"
    />
  </div>
</template>

<style scoped>
#projects {
  display: inline-block;
  margin-top: 60px;
}
</style>
