<script setup>
import { ref } from "vue";

let activeBloc = ref(1);
let experiencesList = ref([
  {
    company: "Hillstone",
    title: "Développeur Frontend",
    date: "Novembre 2024 - Présent",
    tasks: ["En phase de perfectionnement pour ma prochaine mission."],
  },
  {
    company: "ConformIT",
    title: "Développeur Frontend - VueJS",
    date: "Août 2023 - Octobre 2024",
    tasks: [
      "Conception et maintenance d’applications Web complexes, axées sur une interface utilisateur élégante et performante.",
      "Traduction fluide des maquettes en composants interactifs et réactifs.",
      "Participation à des choix architecturaux stratégiques et amélioration continue en équipe Scrum.",
    ],
  },
  {
    company: "VERMEG",
    title: "Développeur Frontend - Angular",
    date: "Juillet 2020 - Juillet 2023",
    tasks: [
      "Développement de la plateforme VEGGO, un outil révolutionnaire pour les solutions numériques en finance.",
      "Implémentation de fonctionnalités robustes, intégration de webservices et optimisation de l’expérience utilisateur.",
      "Rédaction de documentation technique claire et réalisation de tests unitaires de qualité.",
    ],
  },
  {
    company: "GoMyCode",
    title: "Développeur Fullstack - React",
    date: "Octobre 2019 - Mars 2020",
    tasks: [
      "Création de la plateforme d'apprentissage GoMyCode en utilisant le stack MERN.",
      "Conception d’interfaces modernes, réactives et optimisées pour l’éducation en ligne.",
      "Collaboration agile pour garantir des solutions rapides, fiables et sécurisées.",
    ],
  },
]);

const showXp = (id) => {
  activeBloc.value = id;
};
</script>

<template>
  <div id="xp">
    <h2 class="text-highlight-1 section-title">Mes Experiences</h2>
    <div id="left">
      <!-- <p :class="activeBloc === 0 ? 'active' : ''" class="company fw600" @click="showXp(0)">ConformIT</p>
            <p :class="activeBloc === 1 ? 'active' : ''" class="company fw600" @click="showXp(1)">VERMEG</p>
            <p :class="activeBloc === 2 ? 'active' : ''" class="company fw600" @click="showXp(2)">GoMyCode</p> -->

      <p
        v-for="({ company }, index) in experiencesList"
        :class="activeBloc === index ? 'active' : ''"
        class="company fw600"
        @click="showXp(index)"
      >
        {{ company }}
      </p>
    </div>
    <div id="right">
      <template v-for="(job, index) in experiencesList">
        <div
          class="job-details"
          :class="index === activeBloc ? '' : 'hide'"
          :id="'bloc_' + index"
        >
          <h3 class="fw600">{{ job.title }}</h3>
          <span id="date">{{ job.date }}</span>
          <br />
          <div v-if="job.tasks" style="margin-top: 10px">
            <p v-for="task in job.tasks" class="fw600 mtb8">
              <span class="text-highlight-2">✓</span> {{ task }}
            </p>
          </div>
        </div>
      </template>
    </div>
  </div>
</template>

<style scoped>
#xp {
  margin-top: 60px;
}

#xp #left {
  float: left;
  width: 25%;
}

#xp #right {
  float: left;
  width: 75%;
}

#xp #right h3 {
  font-size: 20px;
}

.fw600 {
  font-weight: 600;
}

.mtb8 {
  margin: 8px 0px;
}

#date {
  font-style: italic;
  font-size: 14px;
}

.company {
  border-left: 4px solid var(--vt-c-custom-text-1);
  line-height: 30px;
  padding-left: 10px;
}

.active {
  border-left: 4px solid var(--vt-c-custom-text-2);
  color: var(--vt-c-custom-text-2);
}

.company:hover {
  cursor: pointer;
  color: var(--vt-c-custom-text-1);
}

.hide {
  display: none;
}

@media screen and (max-width: 600px) {
  #xp #right {
    width: 100%;
    margin-top: 20px;
  }

  #xp #left {
    width: 100%;
  }

  .company {
    border: none;
    padding-left: 0px;
    float: left;
    margin-right: 10px;
  }
}
</style>
