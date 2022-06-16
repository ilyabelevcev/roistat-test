<template>
   <div class="content-wrapper">
      <table-wrapper 
         :chiefs="chiefs"
         @add="showDialog"
         :dialog_visible="dialog_visible"/>
      <my-dialog  v-model:show="dialog_visible">
         <form-wrapper
            :chiefs="chiefs"/>
      </my-dialog>
   </div>
</template>

<script>
   import formWrapper from '@/components/form_wrapper.vue'
   import tableWrapper from '@/components/table_wrapper.vue'
   export default {
      components: {
         formWrapper,
         tableWrapper,
      },
      data() {
         return{
            chiefs: [
               {id: 0, name: 'Илья', tel: '+79166869692'},
               {id: 0, name: 'Илья', tel: '+79166869692'},
               {id: 0, name: 'Илья', tel: '+79166869692'},
               {id: 0, name: 'Илья', tel: '+79166869692'},
               {id: 0, name: 'Илья', tel: '+79166869692'},
               {id: 0, name: 'Илья', tel: '+79166869692'},
            ],
            dialog_visible: false,
         }
      },
      methods: {
         showDialog() {
            this.dialog_visible = true;
         },
      }
   }
</script>

<style>
   *,*::after,*::before{
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-size: 24px;
   }
   button{
      cursor: pointer;
   }
   #vue_app{
      max-width: 1920px;
      padding: 0px 5px;
      margin: 0 auto;
   }
   .content-wrapper{
      display: flex;
      justify-content: flex-start;
   }
</style>
