<template>
   <input 
      :value="modelValue"
      @input="updateInput"
      class="form-input">
</template>

<script>
   export default {
      name: 'my-input',
      props: {
         modelValue: [String, Number]
      },
      methods: {
         updateInput(event) {
            this.$emit('update:modelValue', event.target.value)
         }
      }
   }
</script>

<style scoped>
   .form-input{
      width: 280px;
      padding: 7px 14px;
      border: 1px solid #000;
   }
</style>