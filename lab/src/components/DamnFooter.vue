<template><div v-bind:style="footStyle">footer</div></template>

<script>
export default {
  data() {
    return {
      footStyle: {
        color: "green",
        backgroundColor: "lightblue",
        border: "1px solid darkgreen",
        marginTop: "0",
        width: "100%",
        height: "50px",
      },
    };
  },
};
</script>

<style></style>
