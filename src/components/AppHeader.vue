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
                color: blue;
                border-bottom-color: blue;
                }
            }
            }
        }
    }

</style>
