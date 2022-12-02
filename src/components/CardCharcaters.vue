<script>
    export default {
        name: "CardCharacters",
        props: {
            info:Object,
        },
    }
</script>
<template>
    <div class="text-center">
        <div class="color-figures py-3">
        <img class="mb-3"  :src="info.img" :alt="info.name">
        <h6 class="mb-4 fw-bold">{{info.name}}</h6>
        <div class="color-info">{{info.category}}</div>
        <small class="color-info">{{info.status}}</small>          
        </div>
    </div>
</template>


<style lang="scss" scoped>
   .color-figures{
    background-color: #2e3a46;
   }
   
    img{
        width: 9.375rem;
        height: 12.5rem;
        object-fit: cover;
    }
    h6{
        color: #ffff;
    }
    .color-info{
        color: #726f6f;
    }
</style>