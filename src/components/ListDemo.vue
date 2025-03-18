<template>
    <h3>列表渲染</h3>
    <p v-for="(item,index) of names">{{ item }}--{{ index }}</p>  
    <!-- in或者of  item in itme  或者 item of item-->
    <div v-for="item in result">
        <p>{{ item.title }}</p>
        <img :src="item.avator" alt="">
    </div>
    <!-- <div v-for="item in userInfo"> -->
    <div v-for="(value,key,index) of userInfo">
        {{ value }}--{{ key }}--{{ index }}
    </div>
</template>
 
<script>
export default{
    data(){
        return{
            names:["王鹤棣","田曦薇","杨洋","迪丽热巴"],
            result:[
            {
                "id":2261677,
                "title":"你属于耀眼的世界，而我属于另一个世界，有幸同行一时，但注定要分道扬镳。",
                "avator":"https://img1.baidu.com/it/u=2359169592,909734325&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=749",
            },
            {
                "id":2261566,
                "title":"我以后……可能既没有时间陪她，也没钱让她过更好的生活",
                "avator":"https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fsafe-img.xhscdn.com%2Fbw1%2F12c306db-b1ac-48a2-9780-a67d6c2766ee%3FimageView2%2F2%2Fw%2F1080%2Fformat%2Fjpg&refer=http%3A%2F%2Fsafe-img.xhscdn.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1744890569&t=7bc958fd1a6a4c87407f94a0d93eb591",
            },
            {
                "id":2261662,
                "title":"我们的征途是星辰大海，但每一步都踩在泥土里。",
                "avator":"https://i1.hdslb.com/bfs/archive/4ba7a631ac535833bce5c5e4f711e4e1e6503f5f.jpg",
            },
        ],
        userInfo:{
            name:'Mike',
            age:'19',
            sex:'male'
        }
        }
        
    }
}
</script>