<template>
  <v-app>
    <Navbar/>
    <v-main id="container">
      <v-container fluid>
        <router-view></router-view>
      </v-container>
    </v-main>
    <Footer/>
  </v-app>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'
export default {
  name: 'App',
  components:{
    Navbar,
    Footer,
  },
  data: () => ({
    //
  }),
};
</script>

<style>
.v-main {
  background-color: #EEEEEE;
}
</style>