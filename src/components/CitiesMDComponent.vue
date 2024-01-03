<script setup lang="ts">
import {ref,onMounted} from 'vue'
type CountiesProps={
        id:string,
        name:string,
        communes:string[],
        districts:string[]
}
type CityProps={
    id:string,
    name:string,
    capital:string,
    countie:CountiesProps[],
    totalOfcounties:number

}
import Card from '../components/CityCard.vue'
    const cities =ref<CityProps[]>()
    const cities_total =ref()
    
    async function fetchJokes() {
    try {
        const response =await( await fetch('https://cities-ao.onrender.com/api/v1/cities')).json();
        cities.value=response.provinces
        cities_total.value=response.totalOfProvinces
    
    } catch (error) {
        console.error(error);
    }
}
onMounted(() => {
    fetchJokes()
})
</script>

<template>
    <div class="divmain"> 
    <ul>
        <li v-for="item in cities">
            <Card :city="item"  />
        </li>
    </ul>
    </div>
</template>

<style scoped>

.divmain {
    display: flex;
    margin-top: 8px;
    height:100%;
    width: 100%; 
}

.divmain ul{
    display: grid;
    gap: 5px;
    justify-content: center;
    justify-items: center;
    align-self: center;
    box-sizing: border-box;
    grid-template-columns: repeat(3, 1fr);


}
.divmain ul li{
    list-style: none;


}
@media only screen and (max-width: 600px) {
    .divmain ul{
    display: grid;
    width: 100%;
    justify-content: center;
    gap: 3px;
    grid-template-columns: repeat(2, 1fr);


}
}


</style>

