<template>
    <h1>事件传参</h1>
    <p @click="getNameHandler(item,$event)" v-for="(item,index) of names" :key="index">{{ item }}</p>
    </template>
    
    <script>
    export default{
        data(){
            return{
                names:["iwen","ime","frank"]
            }
        },
        //所有的方法或者函数都放在这里
        methods:{
            getNameHandler(name,e){
                console.log(name);
                console.log(e)
                
            }
                
                
            }
        
    }
    </script>