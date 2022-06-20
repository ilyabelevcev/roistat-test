<template>
   <tbody v-if="chiefs.length > 0">
      <table-item
         v-for= "chief in chiefs" 
         :key="chief.id"
         :chief="chief"/>
   </tbody>
   <tbody v-else>
      Пусто
   </tbody>
</template>

<script>
   import tableItem from '@/components/table_users_item.vue'
   export default {
      components: {
         tableItem,
      },
      props: {
         chiefs: {
            type: Array
         }
      }
   }
</script>