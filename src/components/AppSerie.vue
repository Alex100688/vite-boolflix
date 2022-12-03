<script>
import CountryFlag from 'vue-country-flag-next';
export default
    {
        name: "AppSerie",
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
        <img :src="`https://image.tmdb.org/t/p/w342/${ info.poster_path}`">
        <h4>{{ info.name}}</h4>
        <h3>{{ info.original_name}}</h3>
        <CountryFlag :country="dataFlag(info.original_language)" size="bold"/>
        <div>
        <font-awesome-icon v-for="n in vote" icon="fa-solid fa-star"/>
        <font-awesome-icon v-for=" n in 5 - vote" icon="fa-regular fa-star"/>
        </div>
        
    </div>    
</template>


<style lang="scss" scoped>
    
   
</style>