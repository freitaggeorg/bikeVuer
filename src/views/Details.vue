<template>
  <div class="details">
    <h1>
      This is an Details page of Bike
      {{ bikes[$router.currentRoute._value.params.cardID].coreData.model }}
    </h1>
    <h3>Core Data</h3>
    <div
      v-for="(detail, key) in bikes[$router.currentRoute._value.params.cardID]
        .coreData"
      :key="key"
    >
      <div>{{ key }}:</div>
      <div>{{ detail }}</div>
    </div>
    <h3>Components</h3>
    <div
      v-for="(detail, key) in bikes[$router.currentRoute._value.params.cardID]
        .components"
      :key="key"
    >
      <div>{{ key }}:</div>
      <div>{{ detail }}</div>
    </div>
    <div>Router: {{ $router.currentRoute._value.params.cardID }}</div>
  </div>
</template>

<script>
import json from "@/assets/data.js";

export default {
  name: "Details",
  components: {},
  data() {
    return {
      bikes: json.bikes,
    };
  },
  mounted() {},
};
</script>
