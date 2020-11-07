<template>
  <h1> Dc Heros </h1>
  <ul>
   <li v-for="(value, key) in dcHeros" :key="key">{{value.name}}</li>
  </ul>
  <form @submit.prevent="addHero">
  <label>
    <input v-model.trim="newHero" placeholder="Name of hero" />
  </label>
  <button type="submit">Add Hero</button>
  </form>
</template>

<script>
export default {
  methods: {
    addHero() {
     this.dcHeros.push({name: this.newHero}); 
     this. newHero = '';
    }
  },
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