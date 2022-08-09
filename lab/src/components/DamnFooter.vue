<template>
  <div v-bind:style="footStyle">and this is the f@** footer!!!</div>
</template>

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
        display: "flex",
        justifyContent: "flex-end",
        alignItems: "flex-end",
      },
    };
  },
};
</script>

<style></style>
