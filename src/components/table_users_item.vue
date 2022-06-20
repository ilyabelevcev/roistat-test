<template>
   <tr>
      <td>{{chief.name}}</td>
      <td>{{chief.tel}}</td>
   </tr>
</template>

<script>
export default {
   props: {
      chief: {
         type: Object
      }
   }
}
</script>