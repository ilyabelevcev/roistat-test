<template>
   <table border="1" class="table">
      <thead>
         <tr>
            <th>Имя</th>
            <th>Телефон</th>
         </tr>
      </thead>
      <tbody v-if="chiefs.length > 0">
         <tr 
            v-for= "chief in chiefs"
            :key="chief.id"
         >
            <td>{{chief.name}}</td>
            <td>{{chief.tel}}</td>
         </tr>
      </tbody>
      <tbody v-else>
         <tr>
            <td>Пусто</td>
         </tr>
      </tbody>
   </table>
</template>

<script>
export default {
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
      border-collapse: collapse;
   }
   td {
      padding: 24px 0px 4px 20px;
   }
</style>