<template>
   <label class="label">
      <slot></slot>
   </label>
</template>

<script>
export default {
   name: 'my-label',
}
</script>

<style scoped>
   label{
      width: 100%;
      display: flex;
      align-items: center;
      justify-content: space-between;
   }
</style>