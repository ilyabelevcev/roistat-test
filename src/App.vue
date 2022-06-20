<template>
   <div class="content-wrapper">
      <table-wrapper 
         :chiefs="chiefs"
         @open="showDialog"
         :dialog_visible="dialog_visible"/>
      <my-dialog  v-model:show="dialog_visible">
         <form-wrapper
            :chiefs="chiefs"
            @add="addUser"/>
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
               {
                  id: 0,
                  name: 'Илья',
                  tel: '+7 916 686 96 92',
               },
            ],
            dialog_visible: false,
         }
      },
      methods: {
         showDialog() {
            this.dialog_visible = true;
         },
         addUser(chief) {
            this.chiefs.push(chief);
            this.saveUsers();
            this.dialog_visible = false;
         },
         saveUsers() {
            const parsed = JSON.stringify(this.chiefs);
            localStorage.setItem('chiefs', parsed);
         }
      },
      mounted() {
         if (localStorage.getItem('chiefs')) {
            try {
               this.chiefs = JSON.parse(localStorage.getItem('chiefs'));
            } catch(e) {
               localStorage.removeItem('chiefs');
            }
         }
      }
   }
</script>

<style>
   *,*::before,*::after{
   -moz-box-sizing: border-box;
   -webkit-box-sizing: border-box;
   box-sizing: border-box;
   font-size: 24px;
   margin: 0;
   padding: 0;
   border: 0;
   list-style: none;
   text-decoration: none;
   }
   button{
      cursor: pointer;
   }
   #vue_app{
      max-width: 1100px;
      padding: 0px 5px;
      margin: 0 auto;
   }
   .content-wrapper{
      padding-top: 40px;
      display: flex;
      justify-content: flex-start;
   }
   td {
      padding: 24px 0px 4px 20px;
   }
</style>
