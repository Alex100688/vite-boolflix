<script>
import CountryFlag from 'vue-country-flag-next';
export default
    {
        name: "AppMovies",
        components: {
            CountryFlag,
        }, 
        props: {
            info: Object,
        
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
            <div class="special">
                <h4>{{ info.title || info.name}}</h4>
                <h3>{{ info.original_title || info.original_name}}</h3>
                <CountryFlag :country="dataFlag(info.original_language)" size="bold"/>
                <font-awesome-icon class="star" v-for="n in vote" icon="fa-solid fa-star"/>
                <font-awesome-icon class="star-white" v-for=" n in 5 - vote" icon="fa-regular fa-star"/> 
            </div>
    </div>
       
</template>


<style lang="scss" scoped>
    
   img{
    display: block;
    margin: 1.25rem 0;
   }
   img > .special{
    display: none;
   }
    img >.special:hover{
    display: block;
   }
   .star{
    color: yellow;
    border: none;
   }
   .star-white{
    color: white;
    border: black;
   }
   .star, .star-white{
    margin-left: .625rem;
   }
</style>