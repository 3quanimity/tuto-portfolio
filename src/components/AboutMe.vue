<script setup></script>

<template>
  <div id="about-me">
    <h2 class="text-highlight-1 section-title">Présentation</h2>
    <p class="default-text">
      Je suis un
      <span class="text-highlight-2">Développeur Front-End</span> expérimenté,
      avec une solide expérience des frameworks
      <span class="text-highlight-2">Vue, Angular et React</span>. Spécialisé
      dans la création d'applications web centrées sur l'expérience utilisateur,
      en produisant un
      <span class="text-highlight-2">code propre et efficace</span>. Habitué à
      travailler en équipe <span class="text-highlight-2">Agile</span> et à
      participer aux décisions architecturales pour garantir des
      <span class="text-highlight-2">livrables de qualité</span>.
    </p>
    <!-- TODO: Add contact Page -->
    <!-- <p><RouterLink to="/contact">Contactez-moi!</RouterLink></p> -->
  </div>
</template>

<style scoped>
#about-me {
  /* margin-top: 80px; */
}

.default-text {
  text-align: justify;
}

.default-text span {
  font-weight: bold;
}
</style>
