<script>
import AppMovies from './AppMovies.vue';
import { store } from '../store';
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