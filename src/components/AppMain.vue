<script>
import AppMovies from './AppMovies.vue';
import AppSerie from './AppSerie.vue';
import { store } from '../store';
export default
    {
        name: "AppMain",
        components: {
            AppMovies,
            AppSerie,
    },
        data() {
            return {
                store,
        }
    },   
    }
</script>
<template>
    <div>
    <AppMovies v-for="film in store.films" :info="film"/>
    <AppMovies v-for="serie in store.series" :info="serie"/>
    </div>
   
</template>


<style lang="scss" scoped>
   
</style>