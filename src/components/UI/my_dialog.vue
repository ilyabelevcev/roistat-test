<template>
   <div class="dialog-wrapper" v-if="show === true" @click.stop="hideDialog">
      <div @click.stop class="dialog">
         <slot></slot>
         <button v-if="show === true" @click.stop="hideDialog" class="btn-close">&#10006;</button>
      </div>
   </div>
</template>

<script>
   export default {
      name: 'my-dialog',
      props: {
         show: {
            type: Boolean,
            default: false,
         }
      },
      methods: {
         hideDialog() {
            this.$emit('update:show', false)
         }
      }
   }
</script>

<style scoped>
   .dialog-wrapper{
      position: fixed;
      top: 0;
      bottom: 0;
      left: 0;
      right: 0;
      background: rgba(0, 0, 0, 0.5);
      display: flex;
   }
   .dialog{
      position: absolute;
      right: 95px;
      top: 108px;
      background-color: #fff;
      border-radius: 5px;
      min-width: 500px;
      padding: 23px;
   }
   .btn-close{
      font-size: 15px;
      line-height: 1;
      padding: 0;
      border: none;
      background-color: transparent;
      position: absolute;
      top: 30px;
      right: 23px;
   }
</style>