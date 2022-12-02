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
  <form @submit.prevent="$emit('performSearch')">
    <input v-model="store.textArea" type="text" placeholder="Cerca film e serie tv" required>
    <button type="submit">Cerca</button>
  </form>
</template>


<style lang="scss" scoped>
 
</style>