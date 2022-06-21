<template>
   <ul class="table__content-list" v-if="chiefs.length > 0">
      <table-item
         :chief="chief"
         v-for= "chief in chiefs" 
         :key="chief.id"
      />
   </ul>
   <ul v-else>
      <li class="table__item-empty">Пусто</li>
   </ul>
</template>

<script>
   import tableItem from '@/components/table_item.vue'
   export default {
      components: {
         tableItem,
      },
      props: {
         chiefs: {
            type: Array
         }
      },
   }
</script>

<style scoped>
   .table__content-list{
      border-bottom: 1px solid #000;
   }
   .table__item-empty{
      text-align: center;
      border: 1px solid #000;
      padding: 10px;
   }
</style>