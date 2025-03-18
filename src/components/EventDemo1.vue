<template>
<h1>内联事件处理器</h1>
<!-- <button v-on:click="count++">Add</button>-->
<button @click="count++">Add</button>
<p>Count is :{{ count }}</p>
</template>

<script>
export default{
    data(){
        return{
            count:0
        }
    }
}
</script>