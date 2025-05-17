<script setup lang="ts">

import fruhstuckImg from '@/assets/fruhstuck.png'
import mittagessenImg from '@/assets/mittagessen.png'
import dinnerImg from '@/assets/dinner.png'
import snackImg from '@/assets/snack.png'

interface Data {
  carbs: number,
  protein: number,
  fat: number
}

const props = defineProps<{
  title: string,
  carbs: number,
  currentItems: number,
  icon: 'fruhstuck' | 'mittagessen' | 'dinner' | 'snack',
  data: Data
}>()

const icons = {
  fruhstuck: fruhstuckImg,
  mittagessen: mittagessenImg,
  dinner: dinnerImg,
  snack: snackImg,
}

</script>

<template>
  <v-card class="rounded-xl w-100 ma-2 px-8 py-3 justify-center">
    <div class="d-flex pa-4 align-center justify-space-between ga-6">
      <img :src="icons[icon]" style="width: 100px;"/>
      <div class="d-flex-col">
        <h1>{{ props.title }}</h1>
        <h3><strong>{{ carbs }} carbs</strong></h3>
        <h3 style="color: aqua">{{ currentItems }} item</h3>
      </div>
    </div>
    <v-divider>
      <IngredientAdder />
    </v-divider>
    <div class="d-flex-col ma-5 mr-10">
      <div class="d-flex align-center justify-space-between pr-4">
        <v-icon icon="mdi-barley" size="x-large"></v-icon>
        <div class="flex align-start">
          <h4>CARBS</h4>
          <h4>{{ data.carbs }}g</h4>
        </div>
      </div>
      <div class="d-flex align-center justify-space-between">
        <v-icon icon="mdi-fish" size="x-large"></v-icon>
        <div class="flex align-start">
          <h4>PROTEIN</h4>
          <h4>{{ data.protein }}g</h4>
        </div>
      </div>
      <div class="d-flex align-center justify-space-between pr-10">
        <v-icon icon="mdi-water" size="x-large"></v-icon>
        <div class="d-flex  flex-column">
          <h4 class="text-uppercase">Fat</h4>
          <h4>{{ data.fat }}g</h4>
        </div>
      </div>
    </div>
  </v-card>
</template>
