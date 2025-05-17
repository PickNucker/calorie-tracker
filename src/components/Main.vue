<script setup lang="ts">

</script>

<template>
  <NavbarTracker />
  <v-container class="d-flex justify-center" max-width="1000">
    <div class="d-flex ga-5">
      <MenuCards title="Breakfast" icon="fruhstuck" :carbs="0" :currentItems="0"
        :data="{ carbs: 0, protein: 0, fat: 5 }" />
      <MenuCards title="Lunch" icon="mittagessen" :carbs="2" :currentItems="6" :data="{ carbs: 2, protein: 3, fat: 50 }" />
      <MenuCards title="Dinner" icon="dinner" :carbs="4" :currentItems="10" :data="{ carbs: 1, protein: 60, fat: 1 }" />
      <MenuCards title="Snacks" icon="snack" :carbs="4" :currentItems="10" :data="{ carbs: 1, protein: 60, fat: 1 }" />
    </div>
    <!-- <Chart/> -->
  </v-container>
</template>
