<template>
    <div class="container-cards">
        <Card
            v-for="iterator in cardsTeams"
            :icon="iterator.icon"
            :title="iterator.title"
            :description="iterator.description"
            :button1="iterator.button1"
            :button2="iterator.button2"
        />
    </div>

</template>
  
<script setup lang="ts">
   import { ref } from "vue";
   import Card from "@/components/changePage/cards/CardTeam.vue"

const page = ref("TEAM");

const cardsTeams = [
    {
        icon: 'devicon-electron-original colored',
        title: 'React Developers',
        description: '"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam."',
        button1: 'React',
        button2: 'MUI'
    },
    {
        icon: 'devicon-vuejs-plain colored',
        title: 'Vue.js Team',
        description: '"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam."',
        button1: 'Vuejs',
        button2: 'Developer'
    },
    {
        icon: 'devicon-xd-plain colored',
        title: 'Create Designers',
        description: '"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam."',
        button1: 'Vuejs',
        button2: 'Developer'
    },
    {
        icon: 'bi bi-gear-wide-connected',
        title: 'Suport Team',
        description: '"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam."',
        button1: 'Vuejs',
        button2: 'Developer'
    },
    {
        icon: 'bi bi-globe',
        title: 'Digital Marketing',
        description: '"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam."',
        button1: 'Vuejs',
        button2: 'Developer'
    },
    {
        icon: 'bi bi-calendar',
        title: 'Event',
        description: '"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam."',
        button1: 'Vuejs',
        button2: 'Developer'
    },
    {
        icon: 'devicon-figma-plain colored',
        title: 'Figma',
        description: '"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam."',
        button1: 'Vuejs',
        button2: 'Developer'
    },
    {
        icon: 'devicon-electron-original colored',
        title: 'Native Mobile App',
        description: '"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam."',
        button1: 'Vuejs',
        button2: 'Developer'
    },
]

const changePage = (newPage: string) => {
  page.value = newPage;
};
</script>
  
<style scoped lang="scss">
  .container-cards {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    width: 100%;
    gap: 20px;
  }
</style >