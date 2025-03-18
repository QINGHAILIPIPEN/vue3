<template>
    <h3>条件渲染</h3>
    <div v-if="flag">CAN YOU SEE ME</div>
    <div v-else>see me,thanks</div>
    <div v-if="type === 'A'">A</div>
    <div v-else-if="type === 'B'">B</div>
    <div v-else-if="type === 'C'">C</div>
    <div v-else>NOT A/B/C</div>
    <div v-show="flag">v-show</div>
</template>


<script>
export default {
    data(){
        return{
            flag:false,
            type:"D"
        }
    }
}
</script>