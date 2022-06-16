<template>
   <div class="table-wrapper">
      <my-button @click="showDialog" class="btn-add">Добавить</my-button>
      <table-users :chiefs="chiefs"/>
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
            this.$emit('add')
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