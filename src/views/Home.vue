<template>
  <div class="home">
    <div class="cardContainer">
      <BikeCard
        :dataSet="bikes[0]"
        @click="this.$router.push({ name: 'Details', params: { cardID: 0 } })"
      ></BikeCard>
      <BikeCard :dataSet="bikes[0]"></BikeCard>
      <BikeCard :dataSet="bikes[0]"></BikeCard>
      <BikeCard :dataSet="bikes[0]"></BikeCard>
      <BikeCard :dataSet="bikes[0]"></BikeCard>
      <BikeCard :dataSet="bikes[0]"></BikeCard>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
//import HelloWorld from '@/components/HelloWorld.vue'
import BikeCard from "@/components/BikeCard.vue";
import json from "@/assets/data.js";

export default {
  name: "Home",
  components: {
    BikeCard,
  },
  data() {
    return {
      bikes: json.bikes,
    };
  },
  mounted() {},
};
</script>

<style scoped>
.cardContainer {
  display: inline-block;
}
</style>
