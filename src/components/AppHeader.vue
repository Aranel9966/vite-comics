<script >
import AppBookshelf from './AppBookshelf.vue';
export default{
  data(){
    return{
      menuNav:['CHARACTERS','COMICS','MOVIES','TV','GAMES','COLLECTIBLES','VIDEOS','FANS','NEWS','SHOP'],
      comics:[
        {
          thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
          price: "$19.99",
          series: "Action Comics",
          type: "comic book"
        },
        {
          thumb: "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
          price: "$3.99",
          series: "American Vampire 1976",
          type: "comic book"
        },
        {
          thumb: "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
          price: "$16.99",
          series: "Aquaman",
          type: "graphic novel"
        },
        {
          thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
          price: "$2.99",
          series: "Batgirl",
          type: "comic book"
        },
        {
          thumb: "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
          price: "$3.99",
          series: "Batman",
          type: "comic book"
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
          price: "$2.99",
          series: "Batman Beyond",
          type: "comic book"
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
          price: "$3.99",
          series: "Batman/Superman",
          type: "comic book"
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
          price: "$4.99",
          series: "Batman/Superman Annual",
          type: "comic book"
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
          price: "$5.99",
          series: "Batman: The Joker War Zone",
          type: "comic book"
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
          price: "$6.99",
          series: "Batman: Three Jokers",
          type: "comic book"
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
          price: "$4.99",
          series: "Batman: White Knight Presents: Harley Quinn",
          type: "comic book"
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
          price: "$16.99",
          series: "Catwoman",
          type: "graphic novel"
        }
      ],
    startIndex:1
      }  
  },
  components:{
    AppBookshelf
  },
  methods: {
    active(index){
      this.startIndex=index
      console.log(this.startIndex)
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
          <li v-for="(menuLink,index) in menuNav" @click="active(index)" :class="startIndex == index ? 'active' : ''" >{{ menuLink }}</li>
        </ul>
      </div>
    </nav>
    <div id="jumbotron"></div>
    <h1>CURRENT SERIES</h1>
    <div class="container">
      <AppBookshelf v-for="card in comics" :price="card.price" :img="card.thumb" :name="card.series"></AppBookshelf>
      <button>LOAD MORE</button>
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
            img{
              height: 60px;
            }
        };

        .menu {
            display: flex;
            align-items: center;

            ul {
            display: flex;
            flex-direction: row;
            gap: 20px;

            li {
                font-size: small;
                font-weight: bold;
                padding:  40px 0px;
                // border-bottom: 3px solid transparent;

                &:hover {
                cursor: pointer;
                color: #0282f9;
                }
            }
            }
        }
    };
    .container{
      display: flex;
      flex-flow: row wrap;
      justify-content: center;
      width: 1000px;
      margin: 0 auto;
      padding: 50px 20px;
      color: white;
        button{
          
          background-color: #0282f9;
          color: white;
          padding: 15px;
          width: 220px;
          margin: 50px
        }
    };
    #jumbotron{
      background-image: url('../../public/img/jumbotron.jpg');
      height: 400px;

    };
    h1{
      background-color: #0282f9;
      color: white;
      top: -20px;
      left: 20%;
      width: 280px;
      padding: 5px;
      position: relative;

    }
    .active{
      color: #0282f9;
      border-bottom: 3px solid #0282f9;
      }
    
</style>
