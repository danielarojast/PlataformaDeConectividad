<template>
    <div class="bodyHeader">
        <button class="generalFont" @click="ChangePage('PROFILE')" :class="{ activeButton: page === 'PROFILE' }">
            <i class="bi bi-person-check"></i> Profile
        </button>
        <button class="generalFont" @click="ChangePage('TEAM')" :class="{ activeButton: page === 'TEAM' }">
            <i class="bi bi-person-plus"></i> Team
        </button>
        <button class="generalFont" @click="ChangePage('PROJECTS')" :class="{ activeButton: page === 'PROJECTS' }">
            <i class="bi bi-columns-gap"></i> Projects
        </button>
        <button class="generalFont" @click="ChangePage('CONNECTIONS')" :class="{ activeButton: page === 'CONNECTIONS' }">
            <i class="bi bi-paperclip"></i> Connections
        </button>
    </div>


    <div v-if="page === 'PROFILE'">
        <Profile />
    </div>
    <div v-if="page === 'TEAM'">
        <Team />
    </div>
    <div v-if="page === 'PROJECTS'">
        <Projects />
    </div>
    <div v-if="page === 'CONNECTIONS'">
        <Connections />
    </div>

</template>
  
<script setup lang="ts">
    import Profile from "@/components/changePage/Profile.vue";
    import Team from "@/components/changePage/Team.vue";
    import Projects from "@/components/changePage/Projects.vue";
    import Connections from "@/components/changePage/Connections.vue";
    import { ref } from "vue";

    const page= ref("PROFILE");

    const ChangePage = (newPage: string) => {
        page.value = newPage;
      }

</script>
  
<style scoped lang="scss">
.bodyHeader{
    margin: 20px 0;
}
.bodyHeader :hover{
    background-color: #a59ef5;
    color: white;
}
.bodyHeader button{
    margin: 2px;
}

.bodyHeader .activeButton{
    background-color: #7266ee;
    color: white;
}
</style >