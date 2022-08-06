<template>
 <h2>Reaction timer game</h2>
 <button @click="start">Play</button>
 <datainput v-if="isplaying" :delay="delay" :disabled="isplaying"/>
 <result />
</template>

<script>
import datainput from "./components/Block-data.vue";
import result from './components/Result-timer.vue';

export default {
  name: 'App',
  components:{
     datainput,
     result,
  },
  data(){
    return{
        isplaying:false,
        delay:null,
    }
  },
  methods:{
    start(){
        this.isplaying=true;
        this.delay=2000 + Math.random() * 5000;
        console.log(this.delay);
    }
  }
 
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
}
</style>
