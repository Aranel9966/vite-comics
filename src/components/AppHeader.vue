<script >
export default{
  data(){
        return{
            menuNav:['CHARACTERS','COMICS','MOVIES','TV','GAMES','COLLECTIBLES','VIDEOS','FANS','NEWS','SHOP'],

        }
    },

}
</script>

<template>
    <nav>
        <div>

            <img src="/img/favicon.ico" alt="">
        </div>
        <div>
            <ul>
                <li v-for="menuLink in menuNav">{{ menuLink }}</li>
            </ul>
        </div>

    </nav>
</template>

<style lang="scss" >
    nav{
        display: flex;
        justify-content: space-around;
        background-color: white;
        div{
            // width: 100%;
            display: flex;
            align-items: center;
            ul{
                display: flex;
                flex-direction: row;
                li{
                    font-size: small;
                    font-weight: bold;
                    padding: 22px ;  
                    
                    &:hover{
                        cursor: pointer;
                        color: blue;
                        border-bottom: 3px solid blue;
                       
                    }
                }
            }
        }
    }
</style>
