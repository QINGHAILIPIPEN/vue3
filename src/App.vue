<template>
<h1>模板语法</h1>
<p>{{ msg }}</p>
<p>{{ number + 1 }}</p>
<p>{{ ok ? 'yes' : 'no ' }}</p>
<p>{{ message.split('').reverse() }}</p>
<!-- <p>{{ var = 1 }}</p> -->
<!-- <p>{{ if(ok){return message} }}</p> -->
 <p>{{ rawHtml }}</p>
 <p v-html="rawHtml"></p>

</template>

<script>
export default{
  data(){
    return{
      msg:"神奇的语法",
      number:10,ok:true,
      message:"大家好",
      rawHtml:"<a href='https://cn.vuejs.org/guide/quick-start.html'>vue<a/>"
    }
  }
}
</script>


