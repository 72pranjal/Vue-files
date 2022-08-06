<template>
  
  <child v-if="show">
<template v-slot:header>
    <h1>Tom</h1>
</template>
<template v-slot:content>
 <h2>A vue3 product</h2>
</template>
<template v-slot:footer>
   <button class="btn" @click="getdata2">Buy Now</button><br><br>
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
   <button class="btn" @click="getdata1">Buy Now</button><br><br>
</template>
<br><br>
  </child>
  <child><template v-slot:toogle><button  @click="show=!show" class="btn1">Toogle</button></template></child>

  
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
    },
   
}
</script>

<style>
.btn{
    width: 80px;
    height: 30px;
    font-size: 15px;
    background-color: skyblue;
    border-radius: 9px;
    color:blue;
}
.btn1{
    width: 90px;
    height: 40px;
    font-size: 20px;
    background-color:lightcyan;
    border-radius: 7px;
}
</style>