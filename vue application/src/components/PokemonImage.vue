<template>
  <img
    class="pokemonImage"
    :src=imgPath
  />
</template>

<script>

export default {
  name: "PokemonImage",
  props: {
    imgPath: String,
  },
};
</script>

<style>
.pokemonImage {
  grid-area: pokemonImage;
  max-height: 15em;
  width: 100%;
  object-fit: contain;
  background-color: lightgrey;
  border-radius: 0.5em;
}
</style>