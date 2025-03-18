<template>
  <div :class="dynamicClass" v-bind:id="dynamicId">测试</div>
  <button :disabled="isButtonDisabled">button</button>
  <div v-bind="Object">测试</div>
</template>

<script>
export default{
  data(){
    return{
      dynamicClass:"active",
      dynamicId:"appID",
      isButtonDisabled:false,
      Object:{
        class:"active",
        id:"appID"
      }
    }
  }
}
</script>

<style>
.active{
  color:brown;
  font-size: 40px;
}
</style>