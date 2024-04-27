<template>
  <div class="pokemonType">
        <h3 class="typeHeading">Type</h3>
        <div class="typeList">
          <span v-for="t of type" :key="t">{{ t }}</span>
        </div>
      </div>
</template>
    
    <script>
export default {
  name: "PokemonType",
  props: {
    type: Array
  },
};
</script>
    
    <style>
.pokemonType {
  grid-area: pokemonType;
  width: 100%;
}

.typeHeading {
  margin: 0 0 0.5em 0;
  padding: 0;
  text-align: center;
}

.typeList {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  flex-wrap: wrap;
}

.typeList span {
  background-color: #9bcb50;
  width: 30%;
  text-align: center;
  border-radius: 0.5em;
  margin: 0.25em 0;
  padding: 0.1em;
}
</style>