<template>
  <div>

    <!-- //* PRIMA SEZIONE -->


    <div class=" container-fluid">
        <div class="row clearfix bg-grey world-bg">
            <div class="col-6 text-section">
                <h5 class="turquoise">New challenges, new skills</h5>
                <h1>Build your own life coach business</h1>
                <p>Whole-Life Business Coaching for committed entepreneurs</p>
                <button class="turquoise_button">Get started today</button>
            </div>
            <div class="col-5">
                <img class="fr" src="../assets/img/home-business-hero-avatar.png" alt="">
            </div>
        </div>
    </div> 


    <!-- //? SECONDA SEZIONE -->

    <div class="container-fluid section-height">
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





  </div>
</template>

<script>
export default {
    name:'Main',
    data(){
        return{
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
                }
        }
    }

}
</script>

<style lang="scss">
@import "../style/colors.scss";

.section-height{
    height: 100vh;
    padding:100px;
}

.bg-grey{
    background-color: $greybackground;
}

.world-bg{
    background-image: url(../assets/img/home-business-hero-global-image.png);
    background-repeat: no-repeat;
    background-position: 80%;
    background-size: 500px 500px;
}
.row{
    padding: 0 200px;

    .text-section{
        padding-top:150px;
    }

    .turquoise{
        color:$turquoiseTitle;
    }

    p{
        font-size: 0.8rem;
        color:$pColor;
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

    .turquoise_button{
        background-color: $turquoiseButton;
        color: $white;
    }
    .dark_button{
        background-color: $white;
        color:$turquoiseButton;
        border:1px solid $greybackground;
    }

    img{
        height: 70vh;
    }
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