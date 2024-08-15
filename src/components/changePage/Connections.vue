<template>
    <div class="container-cards">
        <Card
            v-for="iterator in cardsTeams"
            :photo="iterator.photo"
            :name="iterator.name"
            :profesion="iterator.profesion"
            :button1="iterator.button1"
            :button2="iterator.button2"
            :nProjects="iterator.nProjects"
            :nConnections="iterator.nConnections"
            :nTasks="iterator.nTasks"

        />
    </div>

</template>
  
<script setup lang="ts">
   import { ref } from "vue";
   import Card from "@/components/changePage/cards/CardConnections.vue"

const page = ref("TEAM");

const cardsTeams = [
    {
        photo: 'perfil.png',
        name: 'Mark Gilbert',
        profesion: 'Developer',
        button1: 'React',
        button2: 'MUI',
        nProjects: '18',
        nConnections: '830',
        nTasks: '290',
    },
    {
        photo: 'perfil.png',
        name: 'Egenia Gilbert',
        profesion: 'Developer',
        button1: 'Angular',
        button2: 'React',
        nProjects: '112',
        nConnections: '2.3k',
        nTasks: '1.80k',
    },
    {
        photo: 'perfil.png',
        name: 'Francis Byrd',
        profesion: 'UI/UX Designer',
        button1: 'Figma',
        button2: 'Sketch',
        nProjects: '32',
        nConnections: '1.25k',
        nTasks: '89',
    },
    {
        photo: 'perfil.png',
        name: 'Leon Johnson',
        profesion: 'Developer',
        button1: 'React',
        button2: 'HTML',
        nProjects: '224',
        nConnections: '23.8k',
        nTasks: '290',
    },
    {
        photo: 'perfil.png',
        name: 'Jane Smith',
        profesion: 'UI/UX Designer',
        button1: 'Photoshop',
        button2: 'Sketch',
        nProjects: '89',
        nConnections: '12.4',
        nTasks: '820',
    },
    {
        photo: 'perfil.png',
        name: 'JuanGilbert',
        profesion: 'Developer',
        button1: 'Spring Boot',
        button2: 'JAVA',
        nProjects: '18',
        nConnections: '830',
        nTasks: '290',
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