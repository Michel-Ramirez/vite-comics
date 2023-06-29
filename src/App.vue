
<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import "@fontsource/open-sans/400.css";
import "@fontsource/open-sans-condensed/400.css";


export default {
  data() {
    return {

    }
  },
  components: {
    AppHeader,
    AppMain,
    AppFooter,
  }
}
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppFooter />
</template>

<style>
body {
  font-family: 'Open Sans', 'Helvetica Neue', sans-serif;
}

.wrapper {
  max-width: 1080px;
  margin: 0 auto;
}

ul {
  list-style-type: none;
}

a {
  text-decoration: none;
  color: black;
}
</style>
