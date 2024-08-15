<template>
    <div class="container-cards">
        <Card
            v-for="iterator in cardsTeams"
            :icon="iterator.icon"
            :title="iterator.title"
            :description="iterator.description"
            :client="iterator.client"
            :hours="iterator.hours"
            :task="iterator.task"
            :percentage="iterator.percentage"
            :members="iterator.members"
        />
    </div>

</template>
  
<script setup lang="ts">
   import { ref } from "vue";
   import Card from "@/components/changePage/cards/CardProjects.vue"

const page = ref("TEAM");

const cardsTeams = [
    {
        icon: 'devicon-electron-original colored',
        title: 'React Developers',
        description: '"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt. "',
        client: 'Christina Jimenez',
        hours: '380/244',
        task:'290/340',
        percentage: 75,
        members: '280'
    },
    {
        icon: 'devicon-vuejs-plain colored',
        title: 'Rocky McDonald',
        description: '"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt. "',
        client: 'Jhon Smith',
        hours: '840/421',
        task:'221/140',
        percentage: 30,
        members: '458'
    },
    {
        icon: 'devicon-xd-plain colored',
        title: 'Create Designers',
        description: '"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt. "',
        client: 'Jerry Smith',
        hours: '98/135',
        task:'12/90',
        percentage: 55,
        members: '1.1k'
    },
    {
        icon: 'bi bi-gear-wide-connected',
        title: 'Suport Team',
        description: '"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt. "',
        client: 'Hulda Wright',
        hours: '290/340',
        task:'380/244',
        percentage: 40,
        members: '280'
    },
    {
        icon: 'bi bi-globe',
        title: 'Digital Marketing',
        description: '"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt. "',
        client: 'Olive Strickland',
        hours: '580/445',
        task:'27/290',
        percentage: 95,
        members: '16'
    },
    {
        icon: 'bi bi-calendar',
        title: 'Event',
        description: '"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt. "',
        client: 'Hulda Wright',
        hours: '380/244',
        task:'290/340',
        percentage: 10,
        members: '137'
    },
    {
        icon: 'devicon-figma-plain colored',
        title: 'Figma',
        description: '"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt. "',
        client: 'Rcky McDonald',
        hours: '784/244',
        task:'290/340',
        percentage: 80,
        members: '520'
    },
    {
        icon: 'devicon-electron-original colored',
        title: 'Native Mobile App',
        description: '"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt. "',
        client: 'Christina Jimenez',
        hours: '380/244',
        task:'290/340',
        percentage: 35,
        members: '280'
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