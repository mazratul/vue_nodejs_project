<template>
  <div class="pokemonPhysicalDetails">
    <span class="height">Height: {{ height }}</span>
    <span class="weight">Weight: {{ weight }} lbs</span>
    <span class="gender" v-if="gender.male && gender.female">Gender: &male;  &female;</span>
    <span class="gender" v-else-if="gender.male && !gender.female">Gender: &male;</span>
    <span class="gender" v-else-if="!gender.male && gender.female">Gender: &female;</span>
    <span class="gender" v-else>Gender: Unknown</span>
    <span class="category">Category: {{ category }}</span>
    <span class="abilities">Abilities: {{ abilities.join(", ") }}</span>
  </div>
</template>
    
    <script>
export default {
  name: "PokemonPhysicalDetails",
  props: {
    height: String,
    weight: Number,
    category: String,
    gender: Object,
    abilities: Array,
  },
};
</script>
    
    <style>
.pokemonPhysicalDetails {
  width: 100%;
  background-color: #2fa7d7;
  border-radius: 0.5em;
  padding: 0.5em 0;
  grid-area: pokemonPhysicalDetails;
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 1fr 1fr 1fr;
  grid-template-areas:
    "height weight"
    "gender category"
    "abilities abilities";
  align-items: center;
  justify-items: center;
  row-gap: 0.5em;
  color: whitesmoke;
}

.height {
  grid-area: height;
}

.weight {
  grid-area: weight;
}

.gender {
  grid-area: gender;
}

.category {
  grid-area: category;
}

.abilities {
  grid-area: abilities;
}
</style>