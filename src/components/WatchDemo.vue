<template>
    <h1>侦听器</h1>
    <p>{{ message }}</p>
    <button @click="ChangeText">
        修改数据
    </button>
</template>

<script>

    export default{
        data(){
            return{
                message:"Hello"
            }
        },
        methods:{
            ChangeText(){
                this.message = "World"
            }
        },
        //侦听器
        watch:{
            //newValue:改变之后地数据
            //oldValue:改变之前地数据
            //函数名必须与侦听地数据对象保持一致
            message(newValue,oldValue){
                //数据发生变化，自动执行地函数
                console.log(newValue,oldValue);
                
            }
        }
    }


</script>