<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import axios from "axios";
import { store } from './store';
export default {
  components:
  { AppHeader,
    AppMain,
    AppFooter     
  },
  data() {
    return {
      store,
    }
  },
  methods: {
    informationData() {
      axios.get('https://api.themoviedb.org/3/search/movie', {
        params: {
          api_key: '37f2b7b1da343584c7b426f0fd22a4db',
          query: this.store.textArea,
          language: 'it-IT',
        }
      }).then((respo) => {
        this.store.films = respo.data.results;
      });  
      axios.get('https://api.themoviedb.org/3/search/tv', {
        params: {
          api_key: '37f2b7b1da343584c7b426f0fd22a4db',
          query: this.store.textArea,
          language: 'it-IT',
        }
      }).then((respo) => {
        console.log(this.store.series)
        this.store.series = respo.data.results;
      });  
    },  
  },
}
</script>
<template>
  <div class="container">
    <AppHeader @performSearch="informationData"/>
    <AppMain/>
    <AppFooter/>
  </div>
</template>


<style lang="scss">
  body{
    background-color: black;
    color: #ffff;
  }
  .container{
    max-width: 62.5rem;
    margin: auto;
  }
</style>
