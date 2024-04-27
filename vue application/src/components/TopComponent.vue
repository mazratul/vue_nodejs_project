<template>
  <div class="intro">
    <h1>Pokémon World Explorer</h1>
  </div>
</template>
  
  <script>
export default {
  name: "TopComponent",
  props: {},
};
</script>
  
  <style>
.intro {
  width: 100%;
  height: 10em;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #e3350c;
}

.intro h1 {
  font-weight: bold;
  font-style: italic;
  color: white;
}
</style>
  