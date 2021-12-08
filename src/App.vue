<template>
  <CardMain/>
</template>

<script>
import CardMain from "./components/CardMain.vue";

export default {
  name: "App",
  components: {
    CardMain,
  },
};
</script>

<style>
:root {
  /* Primary */
  --very-dark-blue: hsl(233, 47%, 7%);
  --dark-desaturated-blue: hsl(244, 38%, 16%);
  --soft-violet: hsl(277, 64%, 61%);

  /* Neutral */
  --white: hsl(0, 0%, 100%);
  --slightly-transparent-white-main-paragraph: hsla(0, 0%, 100%, 0.75);
  --slightly-transparent-white-stat-headings: hsla(0, 0%, 100%, 0.6);
}
* {
  margin: 0;
  padding: 0;
   box-sizing:border-box;
}
html {
  font-size: 62.5%;
 
}

body {
  background-color: var(--very-dark-blue);
  height: 100vh;
  display: grid;
  justify-content: center;
  align-items: center;
}

#app {
  font-family: "Inter", "Lexend Deca", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: var(--white);
  max-width: 90vw;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
