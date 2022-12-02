<script>
export default
    {
        name: "AppMovies", 
        props: {
            info:Object,
       },
    }
</script>
<template>
    <div>
        <h4>{{ info.title}}</h4>
        <h3>{{ info.original_title}}</h3>
        <div>{{info.original_language}}</div>
        <div>{{info.vote_average}}</div>
        
    </div>    
</template>


<style lang="scss" scoped>
    
   
</style>