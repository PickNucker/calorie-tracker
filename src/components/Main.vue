<script setup lang="ts">
import { onMounted, ref } from 'vue';

const searchGrocerieProducts = async () => {
  const response = await fetch('https://world.openfoodfacts.org/api/v2/category/dairy.json', {
    method: 'GET',
    headers: {
      Authorization: 'Basic ' + btoa('off:off')
    },
  })
  const data = await response.json();
  return data.product;
}

let products = ref<any[]>([])

onMounted(() => {

  const getGroceries = async () => {
    try {
      const fetchedProducts = await searchGrocerieProducts();
      products.value = fetchedProducts ?? []

      console.log(products)
    } catch (e: any) {
      console.log(e);
    }
  }
  getGroceries();
})
</script>

<template>
  <NavbarTracker />
  <v-container class="d-flex justify-center" max-width="1000">
    <div class="d-flex ga-5">
      <MenuCards title="Breakfast" icon="fruhstuck" :carbs="0" :currentItems="0"
        :data="{ carbs: 0, protein: 0, fat: 5 }" />
      <MenuCards title="Lunch" icon="mittagessen" :carbs="2" :currentItems="6"
        :data="{ carbs: 2, protein: 3, fat: 50 }" />
      <MenuCards title="Dinner" icon="dinner" :carbs="4" :currentItems="10" :data="{ carbs: 1, protein: 60, fat: 1 }" />
      <MenuCards title="Snacks" icon="snack" :carbs="4" :currentItems="10" :data="{ carbs: 1, protein: 60, fat: 1 }" />
    </div>
    <!-- <Chart/> -->
  </v-container>
</template>
