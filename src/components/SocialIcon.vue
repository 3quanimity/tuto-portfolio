<script setup>
import { defineProps } from 'vue'

const props = defineProps({
    link: String,
    icon: String,
    alt: String
})
</script>

<template>
    <!-- <a href="https://fr.linkedin.com/in/haythem-ben-drissia/" target="_blank">
        <img class="social-img" src="../assets/linkedin.png" alt="">
    </a> -->

    <a :href="props.link" target="_blank">
        <img class="social-img" :src="`/src/assets/${props.icon}`" :alt="props.alt">
    </a>
</template>

<style scoped>
.social-img {
    margin-right: 10px;
    filter: opacity(0.8);
}
</style>
