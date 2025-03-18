<template>
    <h1>内联事件处理器</h1>
    <!-- <button v-on:click="count++">Add</button>-->
    <button @click="addCount">Add</button>
    <p>Count is :{{ count }}</p>
    </template>
    
    <script>
    export default{
        data(){
            return{
                count:0
            }
        },
        //所有的方法或者函数都放在这里
        methods:{
            addCount(){
                //读取到data里面的数据的方法：this.count
                this.count+=1
                
                
            }
        }
    }
    </script>