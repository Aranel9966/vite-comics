<script>
export default{
        data(){
            return{
                                  
            }
        },
        props:{
            img:String,
            name:String,      
        }
    }
</script>
<template>
    <div class="card">
        <div><img :src="img" alt=""></div>
        <div>{{name}}</div>
  
    </div>
</template>
<style lang="scss" scoped>
    .card{
        height: 150px;
        width: 150px;  
        &:hover{

        }
    }
</style>