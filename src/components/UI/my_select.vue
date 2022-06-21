<template>
   <select name="selectParent" class="form__select">
      <option value=""></option>
      <option 
         v-for="chief in chiefs" 
         :key="chief.id" 
         :value="chief.name"
      >
         {{chief.name}}
      </option>
   </select>
</template>

<script>
   export default {
      name: 'my-select',
      props: {
         chiefs: {
            type: Array,
         }
      }
   }
</script>

<style scoped>
   .form__select{
      width: 280px;
      padding: 7px 14px;
      border: 1px solid #000;
   }
</style>