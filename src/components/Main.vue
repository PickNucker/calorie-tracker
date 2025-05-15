<script setup lang="ts">
import NavbarTracker from '@/components/NavbarTracker.vue'
import MenuCards from '@/components/MenuCards.vue'
</script>

<template>
  <NavbarTracker />
  <v-container class="fill-height d-flex justify-center justify-space-between" max-width="800">
    <h1>Hallo</h1>
    <div class="d-flex ga-5">

      <MenuCards title="Breakfast" :carbs="0" :currentItems="0"/>
      <MenuCards title="Lunch" :carbs="2" :currentItems="6"/>
      <MenuCards title="Dinner" :carbs="4" :currentItems="10"/>
    </div>
    <h1>Hallo</h1>
    <!-- <Chart/> -->
  </v-container>
</template>
