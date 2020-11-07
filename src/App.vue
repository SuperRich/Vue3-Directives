<template>
  <h1> Dc Heros </h1>
  <ul>
   <li v-for="(value, key) in dcHeros" :key="key">{{value.name}}</li>
  </ul>
  <form @submit.prevent="dcHeros.push({name: newHero}); newHero = '';">
  <label>
    <input v-model.trim="newHero" placeholder="Name of hero" />
  </label>
  <button type="submit">Add Hero</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      isDisabled: false,
      newHero: "",
      dcHeros: [
       { name: "SuperGirl" }, 
       { name: "Flash" },
       { name: "Batman" },
       { name: "Arrow" }, 
       { name: "Superman" }
        ]
    }
  }
  
}
</script>