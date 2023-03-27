<script >
export default{
  data(){
        return{
            menuMain:[
                {
                    icon:'/public/img/buy-comics-digital-comics.png',
                    name:'DIGITAL COMICS',
                },
                {
                    icon:'/public/img/buy-comics-merchandise.png',
                    name:'DC MERCHANDISE',
                },
                {
                    icon:'/public/img/buy-comics-subscriptions.png',
                    name:'COMIC SHOP LOXATOR'
                },
                {
                    icon:'/public/img/buy-comics-shop-locator.png',
                    name:'SUBSCRIPTION'
                },
                {
                    icon:'/public/img/buy-dc-power-visa.svg',
                    name:'DC POWER VISA'
                }
            ]
        }
    },

}
</script>

<template>
  <div class="menuContainer">
    <ul>
        <li v-for="options in menuMain">
            <img :src="options.icon" alt="">
            
            {{ options.name }}
        </li>
    </ul>
    
    

  </div>
</template>

<style lang="scss">
.menuContainer{
    padding: 30px;
    background-color:#0282f9 ;
    color: white;
    ul{

        display: flex;
        flex-direction: row;
        justify-content: center;
        gap: 35px;

        li{
            display: flex;
            align-items: center;
            gap: 10px;
            img{
                width: 40px;
                height: 50px;
            }
        }
    }
}

</style>
