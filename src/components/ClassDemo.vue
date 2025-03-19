<template>
 <p :class="{'active':isActive,'text-danger':hasError}">Class样式绑定1</p>
 <p :class="classObject">Class样式绑定2</p>
<!-- 数组 -->
 <p :class="[arrActive,arrhasError]">Class样式绑定3</p>
<!--在数组中 有条件地渲染某个class 三元表达式 -->
<p :class="[isActive ? 'active' : '']">Class样式绑定4</p>
<!-- 数组和对象嵌套过程中，只能是数组嵌套对象，不能反其道而行 -->
 <p :class="[isActive ? 'active' : '',{'text-danger':hasError}]">Class样式绑定5</p>
</template>

<script>
export default{
    data(){
        return{
            isActive:true,
            hasError:true,
            classObject:{
                'active':true,
                'text-danger':true
            },
            arrActive:"active",
            arrhasError:"text-danger"
        }
    }
}
</script>

<style>
.active{
 
  font-size: 40px;
}
.text-danger{
    color: red;
}
</style> 