<template>
  <div v-bind:style="navStyle" class="navBar">
    <img src="../assets/logo.png" alt="" />
    <h2>This is a navegation Bar</h2>
    <img src="../assets/logo.png" alt="" />
  </div>
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
        height: "70px",
      },
    };
  },
};
</script>

<style>
.navBar {
  display: flex;
  justify-content: space-around;
}
</style>
