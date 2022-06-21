<template>
   <div class="form__wrapper">
      <form class="form" @submit.prevent>
         <h2 class="form__heading">Добавление пользователя</h2>
         <my-label class="form__label" for="name">
            Имя
            <my-input 
               v-model="chief.name"
               type="text"
               id="name"/>
         </my-label>
         <my-label class="form__label" for="tel">
            Телефон
            <my-input
               v-model="chief.tel"
               type="tel"
               id="tel"/>
         </my-label>
         <my-label class="form__label" for="select">
            Начальник
            <my-select
               id="select"
               :chiefs="chiefs"/>
         </my-label>
         <my-button @click="addUser" class="btn-save">Сохранить</my-button>
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
      data() {
         return{
            chief: {
               name: '',
               tel: '',
            }
         }
      },
      methods: {
         addUser() {
            this.chief.id = Date.now();
            this.$emit('add', this.chief)
            this.chief = {
               name: '',
               tel: '',
            }
         },
      },
   }
</script>

<style scoped>
   .form__wrapper{
      position: relative;
   }
   .form{
      display: flex;
      flex-direction: column;
      align-items: flex-start;
   }
   .form__heading{
      margin-bottom: 20px;
   }
   .form__label:not(:last-child){
      margin-bottom: 30px;
   }
</style>