<script>
import { store } from '../store';
import AppMovies from './AppMovies.vue';
export default
    {
        name: "AppMain",
        components: {
            AppMovies,
    },
    data() {
        return {
            store,
        }
    },   
    }
</script>
<template>
    <AppMovies v-for="film in store.films" :info="film"/>
</template>


<style lang="scss" scoped>
   
</style>