<!-- <script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />
    </div>
  </header>

  <main>
    <TheWelcome />
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style> -->

<!-- <script setup>
import Navbar from './components/Navbar.vue';
import InfoCard from './components/InfoCard.vue';

</script> -->
<template >
  <nav>
    <Navbar  one="Home" two="About" three="Contact" linkone="https://www.google.com" linktwo="https://www.zbio.gq" linkthree="https://www.google.com"/>
  </nav>
  <main>
    <InfoCard />
  </main>
  
<footer>
  <FooterComponent currentyear="2023"/>
</footer>
  
</template>
<script>
import Navbar from './components/Navbar.vue'
import InfoCard from './components/InfoCard.vue'
import FooterComponent from './components/FooterComponent.vue';
  // export default{
  //   name: 'App',
  //   components:{
  //     Navbar, InfoCard
  //   },
  //   data(){
  //     return {
  //       title:'Shahzaib2'
  //     }
  //   }
  // }

    export default{
     
      name: 'App',
      components:{
    Navbar,
    InfoCard,
    FooterComponent
},
     

    }
</script>

<style >
  *{
      margin: 0;
      padding: 0;
  }
  footer{
    width: 100%;
  position: absolute;
  bottom: 85px;

  }
  .main{
    padding-bottom: 0;
    margin: 0;
  }

</style>