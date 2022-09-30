<template>
  <div class="Note">
    <MainNavBar/>
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <AddNote msg="Welcome to Your Vue.js + TypeScript App"/>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import AddNote from '@/components/AddNote.vue';
import MainNavBar from '@/components/MainNavBar.vue';

@Options({
  components: {
    MainNavBar,
    AddNote,
  },
})
export default class HomeView extends Vue {}
</script>

<style scoped>
    .Notes {
        margin: 500px;
    }
</style>
