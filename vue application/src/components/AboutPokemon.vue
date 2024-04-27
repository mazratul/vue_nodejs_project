<template>
  <h1 class="pokemonName">{{ name }}</h1>
  <p class="pokemonDescription">{{ description }}</p>
</template>
  
  <script>
export default {
  name: "AboutPokemon",
  props: {
    name: String,
    description: String,
  },
};
</script>
  
  <style>
.pokemonName {
  grid-area: pokemonName;
  margin-top: 0;
  padding-top: 0;
  width: 100%;
  text-align: center;
}

.pokemonDescription {
  grid-area: pokemonDescription;
  padding-top: 0;
  margin-top: 0;
  width: 100%;
  font-size: 0.9em;
}
</style>