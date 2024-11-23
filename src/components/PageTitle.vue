<script setup>
import SocialIcon from "@/components/SocialIcon.vue";
</script>

<template>
  <div id="top-line">
    <a href="https://fr.linkedin.com/in/haythem-ben-drissia/" target="_blank">
      <img
        id="profile-img"
        src="../assets/haythem-pp.png"
        alt="haythem-profile-pic"
        width="200px"
        height="200px"
      />
    </a>
    <div id="line">
      <p>
        Je suis <span class="text-highlight-1">Haythem Ben Drissia</span>,
        <br />
        Ingénieur Front-End.
      </p>
      <!-- <div id="social">
        <SocialIcon
          link="https://fr.linkedin.com/in/haythem-ben-drissia/"
          icon="linkedin.png"
          alt="linkedin icon"
        />
      </div> -->
    </div>
  </div>
</template>

<style scoped>
#top-line {
  margin-top: 25px;
  width: 100%;
  height: 250px;
}

#top-line #profile-img {
  float: left;
  margin-right: 50px;
}

#top-line #line {
  float: left;
  transform: translateY(15%);
  text-align: center;
}

#top-line p {
  font-size: 42px;
  line-height: 60px;
}

#top-line p span {
  font-weight: bold;
}

#social {
  margin-top: 15px;
}

@media screen and (max-width: 905px) {
  #top-line #profile-img {
    display: none;
  }

  #top-line #line {
    float: none;
    transform: translateY(0%);
  }

  #top-line p {
    font-size: 36px;
  }
}
</style>
