<template>
   <div class="table-wrapper">
      <my-button @click="showDialog" class="btn-add">Добавить</my-button>
      <tu :chiefs="chiefs"/>
   </div>
</template>

<script>
   import tableUsers from '@/components/table_users.vue'
   import tu from '@/components/tableUsers.vue'
   export default {
      components: {
         tableUsers,
         tu
      },
      props: {
         chiefs: {
            type: Array
         },
         dialog_visible: {
            type: Boolean
         },
      }, 
      methods: {
         showDialog() {
            this.$emit('open')
         }
      }
   }
</script>

<style scoped>
   .table-wrapper{
      display: flex;
      flex-direction: column;
      align-items: flex-end;
   }
   .btn-add{
      margin-bottom: 20px;
   }
</style>