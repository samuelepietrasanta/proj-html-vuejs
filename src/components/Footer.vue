<template>
  <footer>
      <div class="container">
          <div class="row">
              <div class="col-6">
                  <ul>
                    <li class="footer-title">Address</li>
                    <li v-for="(elemento, index) in footer_components.address" :key="index"> {{elemento}}</li>
                  </ul>
              </div>
              <div class="col-3">
                  <ul>
                    <li class="footer-title"> Explore </li>
                    <li v-for="(elemento, index) in footer_components.explore" :key="index">{{elemento}}</li>
                  </ul>
              </div>
              <div class="col-3">
                  <ul>
                      <li class="footer-title">Information</li>
                      <li v-for="(elemento,index) in footer_components.information" :key="index">{{elemento}}</li>
                  </ul>
              </div>
              <div class="col-6 d-flex">
                  <i v-for="(elemento,index) in footer_components.socialClasses" :key="index" :class="elemento"></i>

              </div>
          </div>
      </div>
  </footer>
</template>

<script>
export default {
    name:'Footer',
    data(){
        return{
            footer_components:{
                address:{
                    physicalAddress: '382 NE 191st St #87394 Miami, FL 33179-3899',
                    telephone:'+1(305)547-9909 (9am - 5pm EST, Monday- Friday)',
                    email:'support@maxcoach.com',
                },
                socialClasses:{
                    facebook:'fab fa-facebook-f',
                    twitter:'fab fa-twitter',
                    instagram:'fab fa-instagram',
                    linkedin:'fab fa-linkedin',
                },
                explore:['Start here', 'Blog' , 'About us' , 'Success story', 'Courses' , 'Contact us'],
                information:['Membership' , 'Purchase guide' , 'Privacy policy' , 'Terms of service'],
                copyright:'<i class="far fa-copyright"></i> 2020 @Maxcoach, All Right Reserved '

            }
        }
    }

}
</script>

<style lang="scss"> 
@import "../style/colors.scss";

footer{
    height: 40vh;
    background-color: $darkBackground;
    padding:30px;

    .container{

        .row{

            ul{
                list-style-type: none;

                .footer-title{
                    color:$white;
                    font-size:1.1rem;
                    font-weight: bold;
                }

                li{
                    font-size:.7rem;
                    color: $footerColor;
                    margin-bottom:5px;
                }
            }
            i{
                color:$footerColor;
                margin-left: 30px;
                font-size: 1.3rem;
            }
            
        }

        }

        
}

</style>