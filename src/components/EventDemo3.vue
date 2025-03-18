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
            addCount(e){
                //读取到data里面的数据的方法：this.count
                //Vue中的event对象，就是原生JS的Event对象
                console.log(e);
                  e.target.innerHTML = "Add" + this.count
                this.count+=1
                
                
            }
        }
    }
    </script>