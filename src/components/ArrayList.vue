<template>
    <h1>数组变化侦听</h1>
    <button @click="addListHandle">添加数据</button>
    <ul>
        <li v-for="(item,index) of names" :key="index">{{ item }}</li>
    </ul>
    <button @click="concatHandle">合并数组</button>
    <h3>数组1</h3>
    <p v-for="(item,index) of num1">{{ item }}</p>
    <h3>数组2</h3>
    <p v-for="(item,index) of num2">{{ item }}</p>

</template>

<script>
export default{
    data(){
        return{
            names:["iwen","ime","frank"],
            num1:[1,2,3,4,5],
            num2:[6,7,8,9,10]
        }
        
    },
    methods:{
        addListHandle(){
            //引起UI自动更新
            //this.names.push("sakura")
            //不会引起UI自动更新
            this.names.concat(["sakura"])
            //console.log(this.names.concat(["sakura"]));
            this.names = this.names.concat(["sakura"])
            
        },
        concatHandle(){
           this.num1 = this.num1.concat(this.num2)
        }
    }
}
</script>