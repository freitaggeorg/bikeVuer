<template>
  <span v-if="label" class="label"
    >{{ label }} in {{ daysOffset }} {{ dayTerm }}:
  </span>
  <svg width="200px" height="20px">
    <rect x="0" y="0" width="200" height="20" style="fill: white" />
    <rect
      x="0"
      y="0"
      :width="200 * portion"
      height="20"
      :style="{ fill: color }"
    />
    <rect
      x="0"
      y="0"
      width="200"
      height="20"
      style="stroke-width: 1px; stroke: black; fill: none"
    />
  </svg>
</template>

<script>
export default {
  name: "Progress",
  props: {
    label: String,
    start: {
      type: String,
      required: true,
    },
    interval: {
      type: Number,
      required: true,
    },
  },
  data() {
    return {
      today: "",
      portion: 1,
      color: "green",
      daysOffset: 0,
      startDate: "",
      endDate: "",
    };
  },
  methods: {
    calculateData() {
      this.today = Date.now();
      this.startDate = new Date(Date.parse(this.start));
      this.endDate = new Date(this.startDate.getTime());
      this.endDate.setMonth(this.endDate.getMonth() + Number(this.interval));
      this.portion =
        1 - (this.endDate - this.today) / (this.endDate - this.startDate);
      if (this.portion > 0.7) this.color = "yellow";
      if (this.portion > 0.9) this.color = "red";
      this.daysOffset =
        (this.endDate.getTime() - new Date(this.today).getTime()) /
        (1000 * 3600 * 24);
      this.daysOffset = Math.ceil(this.daysOffset);
    },
  },
  mounted() {
    this.calculateData();
  },
  computed: {
    dayTerm() {
      if (this.daysOffset == 1) return "day";
      else return "days";
    },
  },
};
</script>

<style>
.label {
}
</style>
