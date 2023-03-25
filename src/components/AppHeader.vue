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
      <div class="logo">
        <img src="/img/favicon.ico" alt="">
      </div>
      <div class="menu">
        <ul>
          <li v-for="menuLink in menuNav">{{ menuLink }}</li>
        </ul>
      </div>
    </nav>
    <div class="container">
    --Content goes here --
    </div>
</template>

<style lang="scss" >
    nav {
        display: flex;
        justify-content: space-around;
        flex-direction: row;
        background-color: white;

        .logo {
            display: flex;
            align-items: center;
        }

        .menu {
            display: flex;
            align-items: center;

            ul {
            display: flex;
            flex-direction: row;

            li {
                font-size: small;
                font-weight: bold;
                padding: 22px;
                border-bottom: 3px solid transparent;

                &:hover {
                cursor: pointer;
                color: #0282f9;
                border-bottom-color: #0282f9;
                }
            }
            }
        }
    }
    .container{
        color: white;
        height: 80px;
        background-color: #1c1c1c;
        display: flex;
        align-items: center;
        padding-left: 120px;
        font-size: x-large;
        font-weight: bold;
    }
</style>
