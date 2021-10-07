<template>
  <div>
    <div class=" container-fluid">
        <div class="row section clearfix">
            <div class="col-6 text-section">
                <h5 class="turquoise">New challenges, new skills</h5>
                <h1>Build your own life coach business</h1>
                <p>Whole-Life Business Coaching for committed entepreneurs</p>
                <button>Get started today</button>
            </div>
            <div class="col-5">
                <img class="fr" src="../assets/img/home-business-hero-avatar.png" alt="">
            </div>
        </div>
    </div> 
  </div>
</template>

<script>
export default {
    name:'Main',

}
</script>

<style lang="scss">
@import "../style/colors.scss";
.section{
    background-image: url(../assets/img/home-business-hero-global-image.png);
    background-repeat: no-repeat;
    background-color: $greybackground;
    background-position: 80%;
    background-size: 500px 500px;
    padding: 0 150px;

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
        color: $white;
        font-weight: bold;
        padding: 10px;
        background-color: $turquoiseButton;
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
    float:left
}
.fr{
    float: right;
}
</style>