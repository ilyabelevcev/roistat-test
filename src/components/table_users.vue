<template>
   <div class="table">
      <table-heading/>
      <table-list :chiefs="chiefs"/>
   </div>
</template>

<script>
import tableHeading from '@/components/table_heading.vue'
import tableList from '@/components/table_list.vue'
export default {
   components: {
      tableList,
      tableHeading,
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
   }
</style>