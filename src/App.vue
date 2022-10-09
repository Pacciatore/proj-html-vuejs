<template>
  <div id="app">

    <HeaderComponent />
    <MainComponent />
    <FooterComponent />

  </div>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css';

import HeaderComponent from '@/components/HeaderComponent.vue';
import MainComponent from '@/components/MainComponent.vue';
import FooterComponent from '@/components/FooterComponent.vue';

export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent,
    FooterComponent
  }
}
</script>

<style lang="scss">
@import '@/assets/style/variables.scss';
@import url('https://fonts.googleapis.com/css2?family=Fira+Sans:wght@300;400;600;700&display=swap');

#app {
  font-family: 'Fira Sans', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.btn-dark {
  background-color: $tr-shark;

  &:hover {
    background-color: $tr-shark-muted;
    border-color: $tr-shark-muted;
  }

}
</style>
