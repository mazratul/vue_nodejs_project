<template>
  <div class="displayPokemon">
    <div class="pokemonInfo" v-for="pokemon of pokemons" :key="pokemon.id">
      <PokemonImage :imgPath=pokemon.imagePath />
      <AboutPokemon :name=pokemon.name :description=pokemon.description />
      <PokemonPhysicalDetails
        :height=pokemon.height
        :weight=pokemon.weight
        :category=pokemon.category
        :gender=pokemon.gender
        :abilities=pokemon.abilities
      />
      <PokemonType :type=pokemon.type />
      <PokemonWeaknesses :weaknesses=pokemon.weaknesses />
    </div>
  </div>
</template>
  
  <script>
import PokemonImage from "./PokemonImage.vue";
import AboutPokemon from "./AboutPokemon.vue";
import PokemonPhysicalDetails from "./PokemonPhysicalDetails.vue";
import PokemonType from "./PokemonType.vue";
import PokemonWeaknesses from "./PokemonWeaknesses.vue";

export default {
  name: "PokemonDisplay",
  props: {
    pokemons: Array,
  },
  components: {
    PokemonImage,
    AboutPokemon,
    PokemonPhysicalDetails,
    PokemonType,
    PokemonWeaknesses,
  },
};
</script>


<style>
.displayPokemon {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
}

.pokemonInfo {
  margin: 1.5em 0;
  box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;
  background-color: white;
  border-radius: 0.5em;
  max-width: 40em;
  padding: 0.5em;
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: auto;
  grid-template-areas:
    "pokemonImage pokemonName"
    "pokemonImage pokemonDescription"
    "pokemonPhysicalDetails pokemonPhysicalDetails"
    "pokemonType pokemonWeaknesses";
  row-gap: 0.5em;
  column-gap: 0.5em;
}
</style>
  