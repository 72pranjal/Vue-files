<template>
 <div>
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

<style>

</style>