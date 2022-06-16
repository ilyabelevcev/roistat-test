<template>
   <div class="form-wrapper">
      <form class="form" @submit.prevent>
         <h2 class="form-heading">Добавление пользователя</h2>
         <label class="form-label" for="name">
            Имя
            <my-input 
               type="text"
               id="name"/>
         </label>
         <label class="form-label" for="tel">
            Телефон
            <my-input
               type="tel"
               id="tel"/>
         </label>
         <label class="form-label" for="select">
            Начальник
            <my-select
               id="select"
               :chiefs="chiefs"/>
         </label>
         <my-button class="btn-save">Сохранить</my-button>
      </form>
   </div>
</template>

<script>
   export default {
      props: {
         chiefs: {
            type: Array,
         },
      },
   }
</script>

<style scoped>
   .form-wrapper{
      position: relative;
   }
   .form{
      display: flex;
      flex-direction: column;
      align-items: flex-start;
   }
   .form-heading{
      margin-bottom: 20px;
   }
   .form-label{
      width: 100%;
      display: flex;
      align-items: center;
      justify-content: space-between;
   }
   .form-label:not(:last-child){
      margin-bottom: 30px;
   }
</style>