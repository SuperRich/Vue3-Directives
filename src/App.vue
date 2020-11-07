<template>
  <h1> Dc Heros </h1>
  <ul>
   <li v-for="(value, key) in dcHeros" :key="key">{{value.name}}</li>
  </ul>
  <input v-model.trim="newHero" />
  <button>Add Hero</button>
</template>

<script>
export default {
  data() {
    return {
      isDisabled: false,
      newHero: "Aquamannnn",
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