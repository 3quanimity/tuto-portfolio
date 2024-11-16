<script setup>
import PageTitle from "@/components/PageTitle.vue"
import AboutMe from "@/components/AboutMe.vue";
import MyTech from "@/components/MyTech.vue";
import MyExperiences from "@/components/MyExperiences.vue";
import MyProjects from "@/components/MyProjects.vue";
</script>


<template>
    <div>
        <PageTitle />
        <AboutMe />
        <MyTech />
        <MyExperiences />
        <MyProjects />
        <div class="signature">
            <center><a href="https://www.linkedin.com/in/haythem-ben-drissia/" class="text-highlight-1"
                    target="_blank">Haythem Ben
                    Drissia</a></center>

        </div>
    </div>
</template>

<style lang="css" scoped>
.signature {
    margin-top: 20px;
    cursor: pointer;
}
</style>
