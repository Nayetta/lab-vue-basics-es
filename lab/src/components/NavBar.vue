<template>
  <div v-bind:style="navStyle">Hi</div>
</template>

<script>
export default {
  data() {
    return {
      navStyle: {
        color: "green",
        backgroundColor: "lightgreen",
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
