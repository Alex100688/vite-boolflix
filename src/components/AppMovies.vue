<script>
import CountryFlag from 'vue-country-flag-next';
export default
    {
        name: "AppMovies",
        components: {
            CountryFlag,
        }, 
        props: {
            info:Object,
        },
       methods: {
        dataFlag(language) {
            if (language == 'en') {
                return 'gb';
            } else {
                return language;
            }                     
        }
        },
       computed: {
        vote() {
               return Math.ceil(this.info.vote_average / 2);
        }
       },
    }
</script>
<template>
    <div>
        <h4>{{ info.title}}</h4>
        <h3>{{ info.original_title}}</h3>
        <CountryFlag :country="dataFlag(info.original_language)" size="bold"/>
        <div>
        <font-awesome-icon v-for="n in vote" icon="fa-solid fa-star"/>
        <font-awesome-icon v-for=" n in 5 - vote" icon="fa-regular fa-star"/>
        </div>
        <img :src="`https://image.tmdb.org/t/p/w342/${ info.poster_path}`">
        
    </div>    
</template>


<style lang="scss" scoped>
    
   
</style>