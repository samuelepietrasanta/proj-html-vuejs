<template>
  <div id="app">

    <Header />
    <Main />
    <Footer />

    
  </div>
</template>

<script>
import '@fortawesome/fontawesome-free/css/all.css'

import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'


export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  }
}
</script>

<style lang="scss">
@import '~bootstrap/dist/css/bootstrap.min.css';
@import "./style/general.scss";




#app{
  margin-top:10px;
}

</style>

