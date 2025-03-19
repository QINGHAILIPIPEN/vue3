<template>
    <p :style="{color:activeColor,fontSize:activeSize + 'px'}">Style绑定1</p>
    <p :style="StyleObject">Style绑定2</p>
    <!-- 绑定数组 -->
    <p :style="[StyleObject]">Style绑定3</p>
</template>
   
   <script>
   export default{
       data(){
           return{
            activeColor:"green",
            activeSize:30,
            StyleObject:{
                color:"red",
                fontSize:"30px"
            }
           }
       }
   }
   </script>
   
