<script setup lang="ts">
import { onMounted } from 'vue';

const props =defineProps<{
  city: any
}>()



</script>
<template>
    <div class="card">
        <div class="container-card bg-green-box">
          <p class="card-title">{{city.name}}</p>
          <p class="card-description">Cap.: {{ city.capital }}</p>
          <p class="card-description">Municípios: {{ city.totalOfcounties }}</p>
        </div>
    </div>
</template>

  <style scoped>

body {
  background-color: black;
}
.card {
  max-width: 270px;
  border: 0;
  width: 220px;
  
  display: flex;
  flex-direction: column;
  margin-inline: auto;
}

.container-card {
  position: relative;
  border: 1px solid transparent;
  background: linear-gradient(71deg, #080509, #1a171c, #080509);
  background-clip: padding-box;
  border-radius: 25px;
  padding: 14px;
}

.bg-green-box,
.bg-white-box,
.bg-yellow-box,
.bg-blue-box {
  position: relative;
}

.bg-green-box::after,
.bg-white-box::after,
.bg-yellow-box::after,
.bg-blue-box::after {
  position: absolute;
  top: -1px;
  bottom: -1px;
  left: -1px;
  right: -1px;
  content: "";
  z-index: -1;
  border-radius: 25px;
}

.bg-green-box::after {
  background: linear-gradient(71deg, #0d1212, #3da077, #0d1212);
}

.bg-white-box::after {
  background: linear-gradient(71deg, #121013, #b0afb0, #121013);
}

.bg-yellow-box::after {
  background: linear-gradient(71deg, #110e0e, #afa220, #110e0e);
}

.bg-blue-box::after {
  background: linear-gradient(71deg, #0c0a0e, #5f6fad, #0c0a0e);
}

.card-title {
  font-weight: 600;
  color: white;
  letter-spacing: -0.02em;
  line-height: 26px;
  font-style: normal;
  font-size: 16px;
  padding-bottom: 4px;
}

.card-description {
  font-weight: 600;
  line-height: 18px;
  color: hsla(0, 0%, 100%, 0.5);
  padding-bottom: 3px;
  font-size: 14px;
}

@media only screen 
  and (min-device-width: 375px) 
  and (max-device-width: 667px) 
  and (-webkit-min-device-pixel-ratio: 2) { 
    .card {
    border: 0;
    width: 180px;
    display: flex;
    flex-direction: column;
}


}
@media only screen 
  and (min-device-width: 414px) 
  and (max-device-width: 736px) 
  and (-webkit-min-device-pixel-ratio: 3) { 
    .card {
    border: 0;
    width: 190px;
    display: flex;
    flex-direction: column;
}

}

  </style>