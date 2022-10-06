<template>
  <main>

    <JumboComponent />
    <AvadaMessageComponent />
    <LatestNewsComponent />

  </main>
</template>

<script>
import JumboComponent from './content/JumboComponent.vue';
import AvadaMessageComponent from './content/AvadaMessageComponent.vue';
import LatestNewsComponent from './content/LatestNewsComponent.vue';
export default {
  name: "MainComponent",
  components: { JumboComponent, AvadaMessageComponent, LatestNewsComponent }
}
</script>

<style scoped lang="scss">

</style>
