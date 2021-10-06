<template>
  <div>
    <div class=" container section clearfix pr-5">
        <div class="row">
            <div class="col-6">
                <h1 class="fl">PROVA</h1>
            </div>
            <div class="col-6">
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
.section{
    background-image: url(../assets/img/home-business-hero-global-image.png);
    background-repeat: no-repeat;
    background-color: #eceeef;

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