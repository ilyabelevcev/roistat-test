<template>
   <div class="table">
      <div class="table__heading">
         <h2 class="table__title">Имя</h2>
         <h2 class="table__title">Телефон</h2>
      </div>
      <!-- <tul :chiefs="chiefs"/> -->
      <ul class="table__content-list" v-if="chiefs.length > 0">
      <!-- <tui
         v-for= "chief in chiefs" 
         :key="chief.id"
         :chief="chief"/> -->
         <li class="table__item-tr" v-for= "chief in chiefs" :key="chief.id">
            <div class="table__item-tr-wrapper">
               <span class="table__item-td">{{chief.name}}</span>
               <span class="table__item-td">{{chief.tel}}</span>
            </div>
         </li>
      </ul>
      <div v-else>
         Пусто
      </div>
   </div>
</template>

<script>
// import tul from '@/components/tableUsersList.vue'
export default {
   // components: {
   //    tul
   // },
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
   .table__heading{
      display: flex;
      width: 100%;
      border: 1px solid #000;
      border-bottom: none;
   }
   .table__title{
      width: 50%;
      padding: 8px 0px 14px 24px;
   }
   .table__title:not(:last-child){
      border-right: 1px solid #000;
   }
   .table__content-list{
      border-bottom: 1px solid #000;
   }
   .table__item-tr{
      width: 100%;
   }
   .table__item-tr:not(:first-child){
      border-top: none;
   }
   .table__item-tr-wrapper{
      display: flex;
   }
   .table__item-td{
      width: 50%;
      padding: 8px 0px 14px 24px;
      border: 1px solid #000;
      border-bottom: none;
   }
   .table__item-td:not(:first-child){
      border-left: none;
   }
</style>