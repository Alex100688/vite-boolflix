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
  <h1>Boolflix</h1>
  <form @submit.prevent="$emit('performSearch')">
    <input class="search " v-model="store.textArea" type="text" placeholder="Cerca film e serie tv" required>
    <button class="button-search" type="submit">Cerca</button>
  </form>
</template>


<style lang="scss" scoped>
h1{
  text-align: center;
  color: red;
  font-size: 2.5rem;
}
.search{
    border: none;
    font-size: 1.25rem;
    margin-left: .3125rem;
  }
.button-search{
    width: 6.25rem;
    height: 2.5rem;
    border-radius: 15%;
    margin-left: .625rem;
  }
</style>