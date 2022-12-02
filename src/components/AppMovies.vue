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
    }
</script>
<template>
    <div>
        <h4>{{ info.title}}</h4>
        <h3>{{ info.original_title}}</h3>
        <CountryFlag :country="dataFlag(info.original_language)" size="bold"/>
        <div>{{info.vote_average}}</div>
        
    </div>    
</template>


<style lang="scss" scoped>
    
   
</style>