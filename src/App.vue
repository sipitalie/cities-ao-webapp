<script setup lang="ts">
import { RouterView } from 'vue-router'
import FirstComponet from './components/FirstComponet.vue'
</script>

<template>
  <header>
    <img alt="AO logo" class="logo" src="@/assets/iconAo.png" width="125" height="125" />

    <div class="wrapper">
      <FirstComponet msg="Cities-AO" />
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 1rem;
}





@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
   
    flex-wrap: wrap;
  }

}
</style>
