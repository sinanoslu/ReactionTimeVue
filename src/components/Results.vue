<template>
 <p>Reaction time: {{score}} ms</p>
 <h1 class="rank">{{rank}}</h1>
  </template>

<script>
export default {
    props:[
    'score'
    ],
    data(){
        return{
            rank:null
        }
    },
    mounted(){
        if(this.score<250){
            this.rank='Ninja Fingers'
        }else if(this.score<400){
            this.rank='Rapid Reflexes'
        }else{
            this.rank='Snail pace...'
        }
    }
}
</script>

<style>
.rank{
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold;
}
</style>