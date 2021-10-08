<template>
  <div>

    <!-- //* PRIMA SEZIONE -->
    <div class=" container-fluid first-section-container">
        <div class="row clearfix bg-grey world-bg">
            <div class="col-6 text-section">
                <h5 class="turquoise">New challenges, new skills</h5>
                <h1>Build your own life coach business</h1>
                <p>Whole-Life Business Coaching for committed entepreneurs</p>
                <button class="turquoise_button">Get started today</button>
            </div>
            <div class="col-5">
                <img class="fr jumbo-image" src="../assets/img/home-business-hero-avatar.png" alt="">
            </div>
        </div>
    </div> 


    <!-- //? SECONDA SEZIONE -->
    <div class="container-fluid second-section-container ">
        <div class="row">
            <div class="col-12 text-center">
                 <h5 class="turquoise">Let's Dream Big Together</h5>
                 <h3>We are pioneers of the digital approach, using leading-edge technology to simplify
                     procedures and apply executive coaching in the new age of digitalization.
                 </h3>
            </div>
            <div class="col-4" v-for="(elemento, index) in digitalApproach" :key="index">
                <i :class=elemento.iconClass></i>
                <div >
                    <h3>{{elemento.title}}</h3>
                    <p>{{elemento.content}}</p>                  
                </div>                        
            </div>
            <div class="col-6 text-end">
                <button class="dark_button">Learn more</button>
            </div>
            <div class="col-6">
                <button class="turquoise_button">Get Started Today</button>
            </div>

            
        </div>
    </div>


    <!-- //#TERZA SEZIONE -->
    <div class="container-fluid third-section-container">
        <div class="row ">

            <div class="col-12 text-center mb-3">
                <h5 class="turquoise">Let's Dream Big Together</h5>
                <h2>Explore How can I help you</h2>
            </div>

            <div class="col m-2 my_howColumn" v-for="(elemento, index) in HowCanIHelpYouOne" :key="index">
                <img class="ridimensionaImmagine" v-bind:src="require('../assets/img/' + elemento.imageSrc)"  :alt="elemento.title" >
                <h4>{{elemento.title}}</h4>
                <p>{{elemento.paragraph}}</p>
                <button class="dark_button discover-button ">Discover now -></button>
            </div>
            
        </div>
    </div>

    <!-- //! QUARTA SEZIONE -->

    <!-- <div class="container-fluid fourth-section-container">
        <div class="row">
            <div class="col-12 text-center mb-3">
                <h5 class="turquoise">Let's Dream Big Together</h5>
                <h2>Explore How can I help you</h2>
            </div>
            <div v-for="(elemento, index) in HowCanIHelpYouTwo" :key="index" class="col" style="background-image: url (../assets/img/logo.png)">


            </div>
        </div>
    </div> -->





  </div>
</template>

<script>
export default {
    name:'Main',
    data(){
        return{

            /* //?SECONDA SEZIONE */
            digitalApproach:{
                oneToOne:{
                    title:'One to One',
                    content:'Getting the necessary clarity about the current state to help you improve your game.',
                    iconClass:'fas fa-chart-bar'
                },
                Anywhere:{
                    title:'Anywhere',
                    content:'Access to valuable and portable program which allow you to setup an live anywhere you want.',
                    iconClass:'fas fa-globe-americas',
                },
                OnTime:{
                    title:'On Time',
                    content:"puntuality is our top priority because it's an essential criteria to assess a program quality.",
                    iconClass:'fas fa-stopwatch',
                },
                OnlineCourses:{
                    title:'Online Courses',
                    content:'Online business coaching now offers you a very powerful way to empower your business into success.',
                    iconClass:'fas fa-laptop',
                },
                Consulting:{
                    title:'Consulting',
                    content:'You will get a clear sense of direction for your business, through assessment and faster results.',
                    iconClass:'far fa-handshake',
                },
                SelfDevelopment:{
                    title:'Self Development',
                    content:'Business Coaching often keep your focus and develop you both in a professional and personal way.',
                    iconClass:'fas fa-cog'
                }
            },


            /*//#TERZA SEZIONE  */
            HowCanIHelpYouOne:{
                first:{
                    imageSrc:'home-business-service-slide-01-480x298.jpg',
                    title:'Consultative Training',
                    paragraph:'With a coach addressing multiple issues that are off balance, affecting your business in various unconsidered ways.'
                },
                second:{
                    imageSrc:'home-business-service-slide-02-480x298.jpg',
                    title:'Real Deal Coaching',
                    paragraph:'Brings an exceptionally powerful opportunity. Being able to accept, to work with that opportunity.'
                },
                third:{
                    imageSrc:'home-business-service-slide-03-480x298.jpg',
                    title:'Advisor training program',
                    paragraph:'Getting high quality, entepreneur mindset driven online business coaching, is what is readed.'
                }
            },

            /* //!QUARTA SEZIONE */
            /* HowCanIHelpYouTwo:{
                first:{
                    imageSrc:'stock-full-hd-03-443x600.jpg',
                    price:'$40,00',
                    title:'Learning to write as a professional author',
                    lessons:'20',
                    students:'50',
                    paragraph:'Paragafo di prova per la prima sezione'

                },
                second:{
                    imageSrc:'stock-full-hd-03-443x600.jpg',
                    price:'Free',
                    title:'Customer-centric Info-tech Strategies',
                    lessons:'15',
                    students:'20',
                    paragraph:'Paragafo di prova per la seconda sezione'

                },
                third:{
                    imageSrc:'stock-full-hd-04-443x600.jpg',
                    price:'$29,90',
                    title:'Open programming courses for everyone: Phyton',
                    lessons:'30',
                    students:'80',
                    paragraph:'Paragafo di prova per la terza sezione'

                },
                fourth:{
                    imageSrc:'stock-full-hd-06-443x600.jpg',
                    price:'$26,00',
                    title:'Academic listening and note-taking',
                    lessons:'5',
                    students:'110',
                    paragraph:'Paragafo di prova per la quarta sezione'

                } 

             } */
        }
    }

}
</script>

<style lang="scss">
@import "../style/colors.scss";

button{
        border:none;
        border-radius:10px;
        font-weight: bold;
        padding: 10px;
    
}

/* //*PRIMA SEZIONE */
.first-section-container{

    background-color: $greybackground;

    .world-bg{
    background-image: url(../assets/img/home-business-hero-global-image.png);
    background-repeat: no-repeat;
    background-position: 80%;
    background-size: 500px 500px;
    }

    .row{
        padding: 0 200px;

        button{
        border:none;
        border-radius:10px;
        font-weight: bold;
        padding: 10px;
        }
        p{
        font-size: 0.8rem;
        color:$pColor;
        }

        button:hover{
        background-color: $darkBackground;
        color:$white;
        }

        .text-section{
        padding-top:150px;
        }

        .jumbo-image{
        height: 70vh;
        }
    }
}

/* //?SECONDA SEZIONE */
.second-section-container{

    height: 100vh;
    padding:100px;


    .row{
        padding:0 200px;
    }

    button{
        border:none;
        border-radius:10px;
        font-weight: bold;
        padding: 10px;
    }

    button:hover{
        background-color: $darkBackground;
        color:$white;
    }

    .dark_button{
        background-color: $white;
        color:$turquoiseButton;
        border:1px solid $greybackground;
    }
}

/* //#TERZA SEZIONE */
.third-section-container{

    height: 100vh;
    padding:100px;
    background-color: $greybackground;
    

    .row{
        padding:0 200px;
    }
    button{
        border:none;
        border-radius:10px;
        font-weight: bold;
        padding: 10px;
    }
    p{
        font-size: 0.9rem;
        color:$pColor;
    }
    .dark_button{
        background-color: $white;
        color:$turquoiseButton;
        border:1px solid $greybackground;
    }

    .dark_button:hover{
        background-color: $turquoiseTitle;
        color:$white;
    }

    .ridimensionaImmagine{
    width: 100%;
    }

    .my_howColumn{
    background-color: $white;
    border-radius: 20px;
    overflow:hidden;
    }
    .discover-button{
    width:100%
    }


}

.fourth-section-container{
    height: 100vh;
    padding:100px;

    .row{

        .col{
            img{
                width: 150px;
            }
        }

    }
}

.turquoise{
        color:$turquoiseTitle;
}

.turquoise_button{
        background-color: $turquoiseButton;
        color: $white;
}

.clearfix{
    display: table;
    content: '';
    clear: both;
}

.fl{
    float:left;
}
.fr{
    float: right;
}
</style>