<template>
<h1>阻止默认事件</h1>
<a @click.prevent="clickHandle" href="https://www.bilibili.com/">哔哩哔哩</a>
<div @click="clickDiv">
    <div @click.stop="clickP">测试冒泡</div>
</div>
</template>

<script>
export default{
    data(){
        return{

        }
    },
    methods:{
        clickHandle(e){
            //阻止默认事件
           //e.preventDefault();
            console.log('点击了')
        },
        clickDiv(){
            console.log('div')
        },
        clickP(e){
            //阻止事件冒泡
           // e.stopPropagation();
            console.log('p')
        }
    }
}
</script>