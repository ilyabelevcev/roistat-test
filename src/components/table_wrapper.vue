<template>
   <div class="table__wrapper">
      <my-button @click="showDialog" class="btn-add">Добавить</my-button>
      <table-users :chiefs="chiefs"></table-users>
   </div>
</template>

<script>
   import tableUsers from '@/components/table_users.vue'
   export default {
      components: {
         tableUsers,
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
   .table__wrapper{
      display: flex;
      flex-direction: column;
      align-items: flex-end;
   }
   .btn-add{
      margin-bottom: 20px;
   }
</style>