<script setup lang="ts">

defineProps({
  title: String,
  carbs: Number,
  currentItems: Number,
})

</script>


<template>
  <v-card class="flex rounded-xl w-100 ma-2 pr-8">
    <div class="d-flex ma-5 ga-2 align-center">
      <v-icon icon="mdi-coffee" class="pa-2 mr-10" style="font-size: 3.5em;"></v-icon>
      <div class="d-flex-col">
        <h1>{{ title }}</h1>
        <h3><strong>{{ carbs }} carbs</strong></h3>
        <h3 style="color: aqua">{{ currentItems }} item</h3>
      </div>
    </div>
    <v-divider>
      <v-btn class="border rounded-pill">
        <v-icon icon="mdi-plus" size="x-large"></v-icon>
      </v-btn>
    </v-divider>
    <div class="d-flex-col ma-5 mr-10">
      <div class="d-flex align-center justify-space-between pr-4">
        <v-icon icon="mdi-barley" size="x-large"></v-icon>
        <div class="flex align-start">
          <h4>CARBS</h4>
          <h4>0g</h4>
        </div>
      </div>
      <div class="d-flex align-center justify-space-between">
        <v-icon icon="mdi-fish" size="x-large"></v-icon>
        <div class="flex align-start">
          <h4>PROTEIN</h4>
          <h4>0g</h4>
        </div>
      </div>
      <div class="d-flex align-center justify-space-between pr-10">
        <v-icon icon="mdi-water" size="x-large"></v-icon>
        <div class="d-flex  flex-column">
          <h4 class="text-uppercase">Fat</h4>
          <h4>0g</h4>
        </div>
      </div>
    </div>
  </v-card>
</template>
