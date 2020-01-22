<template>
  <v-app style="background-color: white;">
    <Header />        
    <v-content>
      <ContentOne />
    </v-content>
    <Footer />
  </v-app>
</template>
<style>

</style>
<script>
import Header from './components/layouts/Header'
import ContentOne from './components/content/ContentOne'
import Footer from './components/layouts/Footer'
//import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    Header, ContentOne, Footer
  },

  data: () => ({
    //
  }),
};
</script>
<style>
</style>