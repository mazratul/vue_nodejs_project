<template>
    <div class="pokemonWeaknesses">
        <h3 class="weaknessHeading">Weaknesses</h3>
        <div class="weaknessList">
          <span v-for="w of weaknesses" :key="w">{{ w }}</span>
        </div>
      </div>
  </template>
      
      <script>
  export default {
    name: "PokemonWeaknesses",
    props: {
      weaknesses: Array
    },
  };
  </script>
      
      <style>
  .pokemonWeaknesses {
  grid-area: pokemonWeaknesses;
  width: 100%;
}

.weaknessHeading {
  margin: 0 0 0.5em 0;
  padding: 0;
  text-align: center;
}

.weaknessList {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  flex-wrap: wrap;
}

.weaknessList span {
  background-color: #fd7c23;
  width: 30%;
  text-align: center;
  border-radius: 0.5em;
  margin: 0.25em 0;
  padding: 0.1em;
}
  </style>