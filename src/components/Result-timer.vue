<template>
  
  <child v-if="show">
<template v-slot:header>
    <h1>Tom</h1>
</template>
<template v-slot:content>
 <h2>A vue3 product</h2>
</template>
<template v-slot:footer>
   <button>Buy Now</button><br><br>
</template>

  </child>
 <child v-else>
<template v-slot:header>
    <h1>Bob</h1>
</template>
<template v-slot:content>
 <h2>A React js product</h2>
</template>
<template v-slot:footer>
   <button>Buy Now</button><br><br>
</template>
<br><br>
  </child>
  <child><template v-slot:toogle><button  @click="show=!show" >Toogle</button></template></child>

  
</template>

<script>
import child from './Child-data.vue';
export default {
    components:{
        child,
    },
    data(){
        return{
            show:true,
        }
    }
}
</script>

<style>

</style>