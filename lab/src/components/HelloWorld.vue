<template>
  <div v-bind:style="backStyle">
    <h1>👨🏻 Iteración 2</h1>
    <p>{{ num }}</p>
    <p>{{ suma(7, 8) }}</p>
    <p>{{ name() }}</p>
    <h1>🪄 Iteración 3</h1>
    <p v-if="showThis">This is shown with an if</p>
    <p v-show="!showThis">This is shown with a show</p>
    <h1>🐜 🐈 🦅 Iteración 4</h1>
    <div>
      <div v-for="animal in animalObject" :key="animal">
        <h2>{{ animal.animal }} - {{ animal.type }}</h2>
        <p>{{ animal.description }}</p>
      </div>
    </div>
    <h1>🌈 Iteración 5</h1>
    <button :style="buttonStyle" @click="changeColor">
      Change color to {{ butCol }}
    </button>
    <button :style="buttonStyle" @click="booleanChange">Change Boolean</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      num: 8,
      nom: "Noemí",
      showThis: false,
      backStyle: {
        backgroundColor: "yellow",
        border: "1px solid darkgreen",
        marginTop: "0",
        paddingBottom: "50px",
        width: "100%",
      },
      buttonStyle: {
        backgroundColor: "yellow",
        border: "1px solid darkgreen",
        marginTop: "0",
        padding: "20px",
        borderRadius: "30px",
      },
      animalObject: [
        {
          animal: "Hormiga",
          type: "Insecto",
          description: "Animal pequeño con muchas patas",
        },
        {
          animal: "Gato",
          type: "Mamifero",
          description: "Dioses del Olimpo en la tierra",
        },
        {
          animal: "Aguila",
          type: "Pajaro",
          description: "Pajarraco semi-grande con un pico gracioso",
        },
      ],
      butCol: "🟣 pink 🟣",
    };
  },
  methods: {
    suma(a, b) {
      return a + b;
    },
    name() {
      return this.nom.split("").reverse().join("");
    },
    changeColor() {
      if (this.backStyle.backgroundColor == "yellow") {
        this.backStyle.backgroundColor = "pink";
        this.buttonStyle.backgroundColor = "pink";
        this.butCol = "🟠 orange 🟠";
      } else if (this.backStyle.backgroundColor == "pink") {
        this.backStyle.backgroundColor = "orange";
        this.buttonStyle.backgroundColor = "orange";
        this.butCol = "🟡 yellow 🟡";
      } else {
        this.backStyle.backgroundColor = "yellow";
        this.buttonStyle.backgroundColor = "yellow";
        this.butCol = "🟣 pink 🟣";
      }
    },
    booleanChange() {
      this.showThis = !this.showThis;

      // if (this.showThis == false) {
      //   this.showThis = true;
      // } else {
      //   this.showThis = false;
      // }
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
