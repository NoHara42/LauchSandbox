<template>
  <div class="container">
      <img class="responsiveLauch bounce" src="../assets/JustLauch.png"/> 
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class HelloWorld extends Vue {
  //this is where you put your code
  
  // @Prop() private msg!: string;

  ScrollNext () {
    alert("hello");
  }
}



</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .container {
        display: flex;
        justify-content: center;
        margin-right: 15px;
        align-items: center;
    }
    .responsiveLauch {
        max-width: 5%;
        height: auto;
    }
    .bounce {
        animation: bounce 2s;
        /* animation-delay: 1s; */
        animation-iteration-count: infinite;
    }
    @keyframes bounce {
        0%,
        25%,
        50%,
        75%,
        100% {
           transform: translateY(0);
        }
        40% {
            transform: translateY(-80px);
        }
        60% {
            transform: translateY(-42px);
        }
    }
</style>
