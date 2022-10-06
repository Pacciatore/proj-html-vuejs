<template>
  <main>

    <JumboComponent />
    <AvadaMessageComponent />

  </main>
</template>

<script>
import JumboComponent from './content/JumboComponent.vue';
import AvadaMessageComponent from './content/AvadaMessageComponent.vue';
export default {
  name: "MainComponent",
  components: { JumboComponent, AvadaMessageComponent }
}
</script>

<style scoped lang="scss">

</style>
