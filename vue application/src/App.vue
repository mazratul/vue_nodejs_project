<template>
  <ErrorComponent v-if="errorOccurred" />
  <template v-else>
    <TopComponent />
    <PokemonDisplay :pokemons="pokemons" />
  </template>
</template>

<script>
import TopComponent from "./components/TopComponent.vue";
import PokemonDisplay from "./components/PokemonDisplay.vue";
import ErrorComponent from "./components/ErrorComponent.vue";

export default {
  name: "App",
  components: {
    TopComponent,
    PokemonDisplay,
    ErrorComponent,
  },
  data() {
    return {
      errorOccurred: false,
      pokemons: [],
    };
  },
  methods: {
    async fetchPokemons() {
      try {
        const res = await fetch(
          "https://ratul-mazumder-porfolio.netlify.app/api"
        );
        const data = await res.json();
        return data;
      } catch (error) {
        this.errorOccurred = true;
      }
    },
  },
  async created() {
    this.pokemons = await this.fetchPokemons();
  },
};
</script>

<style>
* {
  box-sizing: border-box;
}

body {
  background-color: snow;
  margin: 0;
  font-family: "Montserrat", sans-serif;
}
</style>
