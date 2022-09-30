<template>
  <MainNavBar/>
  <div class="about">
    <h1>This is an about page</h1>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import MainNavBar from '@/components/MainNavBar.vue';

@Options({
  components: {
    MainNavBar,
  },
})
export default class AboutView extends Vue {}
</script>
