<template>
    <div>
        <p>Reaction time: {{score}} ms</p>
        <p class="rank">{{rank}}</p>
    </div>
</template>

<script>
    export default {
        name: 'Results',
        props: ['score'],
        data(){
            return{
                rank: null
            }
        },
        mounted(){
            if(this.score < 250){
                this.rank = "You are fast cowboy :)";
            }
            else if(this.score < 400){
                this.rank = "You are fast"
            }else{
                this.rank = "Snail pace..."
            }
        }
    }
</script>

<style scoped>
.rank{
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold;
}
</style>