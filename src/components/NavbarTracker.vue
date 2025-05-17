<script>

</script>


<template>
  <div class="py-16 px-6 ma" style="background: linear-gradient(to right, #e65100, #ffcc80);">
    <div class="d-flex justify-space-between align-center">
      <h1 class="ml-16 text-white font-weight-light">My Food Tracker</h1>
      <div class="d-flex align-center ga-10">
        <div class="d-flex flex-column align-center text-white">
          <v-icon icon="mdi-food" size="x-large" />
          <h3 class="text-center font-weight-light">TOTAL<br /> 0g cals</h3>
        </div>
        <div class="d-flex flex-column align-center text-white ">
          <v-icon icon="mdi-barley" size="x-large" />
          <h3 class="text-center text-uppercase font-weight-light">Carbs<br />0g</h3>
        </div>
        <div class="d-flex flex-column align-center text-white">
          <v-icon icon="mdi-fish" size="x-large" />
          <h3 class="text-center text-uppercase font-weight-light">Protein<br />0g</h3>
        </div>
        <div class="d-flex flex-column align-center text-white">
          <v-icon icon="mdi-water" size="x-large" />
          <h3 class="text-center text-uppercase font-weight-light">Fat<br />0g</h3>
        </div>
        <div class="d-flex align-center justify-center" style="width: 150px; height: 150px;">
          <!-- <img src="@/assets/oval.png" style="width: 150px; height: 150px; color: orangered;" /> -->
          <div class="position-absolute text-center rounded-pill pa-8" style="border: 1.5px solid red;">
            <h1 class="font-weight-light">1500</h1>
            <span>cals left</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
