<template>
   <div class="table__heading">
      <h2 class="table__title">Имя</h2>
      <h2 class="table__title">Телефон</h2>
   </div>
</template>

<style scoped>
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
</style>