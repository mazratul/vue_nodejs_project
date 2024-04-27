<template>
  <div class="errorBox">
    <h1 class="errorStatus">Oops!</h1>
    <p class="errorMessage">
      Error loading Pokémons you were looking for!
    </p>
  </div>
</template>
    
    <script>
export default {
  name: "ErrorComponent",
};
</script>
    
    <style>
.errorBox {
  height: 100vh;
  margin: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.errorStatus {
  text-align: center;
  font-size: 10em;
  margin: 0;
}
.errorMessage {
  text-align: center;
  font-size: 2em;
  margin: 0;
}
</style>