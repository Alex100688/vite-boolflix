<script>
import SectionSelect from './SectionSelect.vue';
import SectionCharacters from './SectionCharacters.vue';
export default
    {
        name: "AppMain",
        components: {
           SectionSelect,
            SectionCharacters,
    },
       
    }
</script>
<template>
    <div class="container bg-white px-4 my-3">
        <div class="row">
            <div class="col-12 py-3">
                <h4 class="ps-3">Found 62 characters</h4>
            </div>
            <SectionCharacters class="my-3"/>
        </div>
       
    </div>
</template>


<style lang="scss" scoped>
   h4{
        background-color: #212529;
        color: #ffff;
    }
</style>