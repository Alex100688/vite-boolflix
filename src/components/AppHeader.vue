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
    <button>Cerca</button>
</template>


<style lang="scss" scoped>
 
</style>