<template>
  <svg width="200px" height="20px">
    <rect x="0" y="0" width="200" height="20" style="fill: red" />
  </svg>
</template>

<script>
export default {
  name: "Progress",
  props: {
    start: Date,
    end: Date
  },
  methods: {}
};
</script>

<style></style>
