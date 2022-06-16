<template>
   <button class="btn">
      <slot></slot>
   </button>
</template>

<script>
   export default {
      name: 'my-button'
   }
</script>

<style scoped>
   .btn{
      padding: 8px 30px;
      border: 1px solid #000;
      border-radius: 20px;
   }
</style>