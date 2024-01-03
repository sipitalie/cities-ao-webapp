<script setup lang="ts">
defineProps<{
  msg: string
}>()


</script>

<template>
  <div class="greetings">
    
    <h1 class="green">{{ msg }}</h1>
    
    <h3>
      Conheça as cidades de Angola e os seus respectivos distritos, zonas e comunas.
      <br>
      <span>[for developers]</span>
      <br>
      <a href="https://github.com/sipitalie/citiesAO" target="_blank" rel="noopener">Tenha acesso à nossa API</a>
    </h3>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
