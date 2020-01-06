<template>
  <v-app>
    <Header />        
    <v-content>
      <ContentOne />
    </v-content>
  </v-app>
</template>
<style>

</style>
<script>
import Header from './components/layouts/Header'
import ContentOne from './components/content/ContentOne'
//import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    Header, ContentOne
  },

  data: () => ({
    //
  }),
};
</script>
<style>
</style>