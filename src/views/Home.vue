<template>
  <div class="home">
    <h1>Bikes</h1>
    <div v-for="(bike, key) in bikes" :key="key">
      <img :src="bike.coreData.image" width="200" height="400" />
      <div>{{ bike.coreData.model }} from {{ bike.coreData.manufacturer }}</div>
      <div>Year: {{ bike.coreData.date_of_pruchase }}</div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
//import HelloWorld from '@/components/HelloWorld.vue'
import json from "@/assets/data.js";

export default {
  name: "Home",
  components: {},
  data() {
    return {
      bikes: json.bikes
    };
  },
  mounted() {}
};
</script>
