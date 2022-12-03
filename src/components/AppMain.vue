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
    <Section>
        <h2>FILM</h2>
        <AppMovies v-for="film in store.films" :info="film"/>
    </Section>
    <section>
        <h2>SERIE TV</h2>
        <AppMovies v-for="serie in store.series" :info="serie"/>
    </section>
</template>


<style lang="scss" scoped>
   
</style>