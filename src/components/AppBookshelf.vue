<script>
export default{
        data(){
            return{
                                  
            }
        },
        props:{
            img:String,
            name:String,      
            price:String,
        }
    }
</script>
<template>
    <div class="card">
        <div class="opacity">
            <div><img :src="img" alt="" /></div>
        </div>
        <div>{{ name }}</div>
        <div class="style-price">{{ price }}</div>
    </div>
</template>
<style lang="scss" scoped>
    .card{
        height: 270px;
        width: 150px;  
        margin: 5px;
        position: relative;

        img{
            width: 150px;
            height: 200px;
            object-fit: cover
        };
        &:hover {
            cursor: pointer;
            transform: scale(1.2);
            .style-price {
                display: block;
                color: greenyellow;
            }
        }
        .opacity:hover {
            opacity: 0.3;
            };
    }
    .style-price{
            position: absolute;
            display: none;
            left: 50%;
            top: 40%;
            transform:translate(-50%,-50%) ;
          
        };
    
</style>