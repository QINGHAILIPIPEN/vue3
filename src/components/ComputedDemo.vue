<template>
<h3>{{ WorldCup }}</h3>
<p>{{ WorldCupContent }}</p>
<p>{{ WorldCupContents() }}</p>
</template>

<script>

export default { 
    data(){
        return{
            WorldCup:{
                country:"Argentina",
                player:["Messi","Lautaro","Dibu"]
            }
        }
    },
    //计算属性
    computed:{
        WorldCupContent(){
            return this.WorldCup.player.length > 0 ? "Yes" : "No"
        }
    },
    //放函数或者方法
    methods:{
        WorldCupContents(){
            return this.WorldCup.player.length > 0 ? "Yes" : "No"
        }
    }
}
</script>