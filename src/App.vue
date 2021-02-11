<template>
  <!-- TITRE -->
  <div id="app">
    <img src="./assets/snk.png" alt="">
    <h1>SASAGEYO</h1>


    <!-- Compteur  -->
    <div id="counter">
      Nombre de recrues : {{ counter }}
    </div>

    <!-- Conditional -->
    <div id="conditional">
      <span v-if="clicks>10">Calme-toi stp</span>
      <div v-if="clicks>50">Mec respire wtf</div>
    </div>

    <!-- Action au clic -->
    <button v-on:click="clicked" id="clicks">
      Clicks: {{ clicks }}
    </button>

    <!-- Input qui injecte le texte en titre -->
    <h2>{{ message }}</h2>
    <input v-model="message"/>
  </div>

  <!-- ALERTE -->

</template>

<script>
export default {
  name: 'App',
  components: {
  },
  data(){
    return {
      counter:0,
      clicks:0,
      message: "Salut !",
    }
  },
  mounted() {
    setInterval(() =>{
      this.counter++
    },3000)
  },
  methods : {
    clicked(){
      this.clicks++;
    }
  },
  
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  background-image: radial-gradient(circle, #ffffff, #efeffb, #dbe0f7, #c4d3f4, #a9c6f0);
}
</style>
