<template>
 <div class="code">
  <header>
    <slot name="header"></slot>
  </header>
  <content>
    <slot name="content"></slot>
  </content>
  <footer>
    <slot name="footer"></slot>
  </footer>
  <slot name="toogle"></slot>
 </div>
 
</template>

<script>
export default {
}
</script>

<style scoped>
 .code{
  border: 2px solid black;
  width: 300px;
  background-color: lightgreen;
  color: red;
  margin-left: auto;
  margin-right: auto;
 }
 .btn{
    width: 400px;
}
</style>