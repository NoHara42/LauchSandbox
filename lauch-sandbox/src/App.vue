<template>
  <div id="app">
    <div class="container">
        <section id="landing-page">
          <LauchLogo class="header" />
          <LauchSymbol class="footer" />
        </section>
        <section id="about1">
          <h1> A WG brand. :) </h1>
        </section>
        <section id="about2">
          <h1 class="top"> Inspired by these lovely people: </h1>
          <div class="gallery">
            <img class="polaroids" id="curtains" src="./assets/curtains.jpg">
            <img class="polaroids" id="toiletWin" src="./assets/toiletWin.jpeg">
          </div>
        </section>
        <section id="about3">
          <h1 class="top"> Auf Balkonien! </h1>
          <div class="gallery">
            <img class="polaroids" id="origin" src="./assets/lauchAufBalkonien.jpg">
            <img class="polaroids" id="balkonien" src="./assets/balkonien.jpg">
          </div>
        </section>
        <section id="tshirts">
          <h1 class="top"> Oolala.</h1>
          <div class="gallery">
            <img class="polaroids" id="tshirt1" src="./assets/tshirtJustLauch.png">
            <img class="polaroids" id="tshirt2" src="./assets/tshirtLAUCH1.png">
            <img class="polaroids" id="tshirt3" src="./assets/tshirtLAUCH2.png">
            <img class="polaroids" id="tshirt4" src="./assets/tshirtLAUCH3.png">
          </div>
        </section>
        <section id="callToAction">
          <h1 class="top"> Angelockt?. <p></p> Send us mail!</h1>
          <div class="gallery">
            <a href="mailto:mailned42@gmail.com?subject=Bitte bitte kann ich ein T-Shirt haben">
              <img src="./assets/mail-letter.png" >
            </a>
          </div>
        </section>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import LauchLogo from "./components/LauchLogo.vue";
import LauchSymbol from "./components/LauchSymbol.vue";

@Component({
  components: {
    LauchLogo,
    LauchSymbol
  }
})
export default class App extends Vue {

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
html, body {
  height: 100vh;
  overflow: hidden;
}
* {
  margin: 0;
  padding: 0;
}
.container {
  height: 100vh;
  overflow: scroll;
  scroll-behavior: smooth;
  scroll-snap-type: y mandatory;
}
section {
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  flex-direction: column;
  width: 100%;
  height: 100%;
  scroll-snap-align: center;
}
.header {
  height: 60%;
  width: 100%;
}
.footer {
  height: 40%;
  width: 100%;
}
@import url('https://fonts.googleapis.com/css?family=Dokdo&display=swap');

h1 {
  font-family: 'Dokdo', cursive;
  font-size: 40px;
  color: darkgreen;
}
.gallery {
  max-width: 100%;
  height: auto;
  display: flex;
  flex-direction: row;
  align-content: center;
  justify-content: space-evenly;
}
.polaroids {
  justify-self: center;
  border-radius: 50%;
  max-width: 40%;
  height: auto;
}

@media only screen and (max-width: 1024px) {
  .h1 {
    font-size: 15px;
    height: 40vh;
  }
  .gallery {
    display: flex;
    height: 60vh;
    flex-direction: column;
    align-content: center;
    justify-content: space-between;
  }
  .polaroids {
    margin-top: 30px;
    align-self: center;
    border-radius: 50%;
    max-width: 40%;
    height: auto;
  }
}
</style>
