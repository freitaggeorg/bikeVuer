<template>
  <div class="outer">
    <div class="imgContainer">
      <img :src="imagePath" />
    </div>
    <div class="textboxContainer">
      <div class="textbox">Model: {{ model }}</div>
      <div class="textbox">Hersteller: {{ manufacturer }}</div>
      <div class="textbox">Year: {{ year }}</div>
      <Progress
        label="Tubeless Intervall"
        :start="this.dataSet.components.wheels.tires.front.tube.last_refill"
        :interval="this.dataSet.components.wheels.tires.front.tube.interval"
      ></Progress>
    </div>
  </div>
</template>

<script>
import Progress from "@/components/Progress.vue";

export default {
  name: "BikeCard",
  components: {
    Progress,
  },
  data() {
    return {
      model: "Testmodel",
      manufacturer: "Testhersteller",
      year: "2020/01/01",
      imagePath: "",
    };
  },
  props: {
    dataSet: Object,
  },
  methods: {
    setData() {
      this.model = this.dataSet.coreData.model;
      this.manufacturer = this.dataSet.coreData.manufacturer;
      this.year = this.dataSet.coreData.date_of_pruchase;
      this.imagePath = this.dataSet.coreData.image;
    },
  },
  mounted() {
    this.setData();
  },
};
</script>

<style>
.outer {
  border: 1px solid black;
  width: 100%;
  height: 100%;
  padding: 10px;
  margin: 10px;
}

progress {
  background-color: #f3f3f3;
  border: 0;
  height: 18px;
  border-radius: 9px;
}

img {
  width: auto;
  height: 250px;
  object-fit: cover;
  object-position: top center;
}
</style>
