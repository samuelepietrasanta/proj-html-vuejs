<template>
  <header class="d-flex justify-content-between align-items-center">
      <img src="../assets/img/dark-logo.png" alt="">
      <nav class="d-flex">
          <ul class="d-flex ">
              <li class="p-2" v-for="(item, index) in nav_menu" :key="index">{{item}} <i class="fas fa-chevron-down"></i></li>
          </ul>
      </nav>
      <div class="language d-flex">
          <img src="../assets/img/en.png" alt="no">
          <p>{{languages.english.language}} </p>
          <i class="fas fa-chevron-down "></i>
          <i class="far fa-user-circle ms-2"></i>
      </div>

      <div class="searchbar d-flex">
          <input type="text" placeholder="Search...">
          <button><i class="fas fa-search"></i></button>
      </div>
      
  </header>
</template>

<script>
export default {
    name:'Header',


    data: function(){
        return{
            nav_menu:['Home' , ' Pages', 'Courses', 'Features', 'Blog', 'Shop' ],
            languages:{
                english:{
                    language:'ENGLISH',
                    flag:'en.png'
                },
                francaise:{
                    language:'FRANCAISE',
                    flag:'fr.png'

                },
                deutch:{
                    language:'DEUTCH',
                    flag:'de.png'

                }
            }
        }
        
    }

}
</script>

<style lang="scss">

header{
    height: 50px;
    padding:25px 125px;

    img{
            height: 20px;
        }

    nav{

        ul{
            list-style-type: none;

            li{
                font-size: .8rem;
            }

        }

    }

    .language{
        height: 50px;
        width:50px;

        img{
            width: 25px;
        }

    }

    .searchbar{
        height: 25px;
    }
}

</style>