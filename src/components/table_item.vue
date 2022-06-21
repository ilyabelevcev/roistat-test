<template>
   <li class="table__item-tr">
      <div class="table__item-tr-wrapper">
         <span class="table__item-td">{{chief.name}}</span>
         <span class="table__item-td">{{chief.tel}}</span>
      </div>
   </li>
</template>

<script>
export default {
   name: 'tableItem',
   props: {
      chief: {
         type: Object
      }
   },
}
</script>

<style scoped>
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