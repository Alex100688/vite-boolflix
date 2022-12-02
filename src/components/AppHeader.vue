<script>
import { store } from "../store";
export default {
  name: "AppHeader",  
  data() {
    return {
      store,
    }
  },
}
</script>
<template>
    <input v-model="store.texArea" type="text" placeholder="Cerca film e serie tv">
    <button @click="$emit('performSearch')">Cerca</button>
</template>


<style lang="scss" scoped>
 
</style>