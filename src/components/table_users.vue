<template>
   <table border="1" class="table">
      <table-heading></table-heading>
      <table-list :chiefs="chiefs"/>
   </table>
</template>

<script>
import tableHeading from '@/components/table_users_heading.vue'
import tableList from '@/components/table_users_list.vue'
export default {
   components: {
      tableHeading,
      tableList,
   },
   props: {
      chiefs: {
         type: Array
      },
   }
}
</script>

<style scoped>
   .table{ 
      width: 500px;
      border-collapse: collapse;
   }
</style>