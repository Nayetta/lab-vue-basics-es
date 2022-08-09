<template>
  <div>
    <h1>Iteraction 2</h1>
    <p>{{ num }}</p>
    <p>{{ suma(7, 8) }}</p>
    <p>{{ name() }}</p>
    <h1>Iteraction 3</h1>
    <p v-if="showThis">This is shown with an if</p>
    <p v-show="!showThis">This is shown with a show</p>
    <h1>Iteraction 4</h1>

    <h1>Iteraction 5</h1>
    <button></button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      num: 8,
      nom: "Noemí",
      showThis: false,
    };
  },
  methods: {
    suma(a, b) {
      return a + b;
    },
    name() {
      return this.nom.split("").reverse().join("");
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
