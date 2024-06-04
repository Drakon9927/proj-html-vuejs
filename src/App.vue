<template>
  <div id="app">
    <AppMain/>
    <AppFooter/>
  </div>
</template>

<script>
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppMain,
    AppFooter
  }
};
</script>