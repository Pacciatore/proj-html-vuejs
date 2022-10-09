<template>
  <main>

    <JumboComponent />
    <AvadaMessageComponent />
    <LatestNewsComponent />
    <BlackBannerComponent :text="'Read our blog'" />

    <BlackBannerComponent :text="'Go to our forum'" />


  </main>
</template>

<script>
import JumboComponent from './content/JumboComponent.vue';
import AvadaMessageComponent from './content/AvadaMessageComponent.vue';
import LatestNewsComponent from './content/LatestNewsComponent.vue';
import BlackBannerComponent from './contentUtils/BlackBannerComponent.vue';
export default {
  name: "MainComponent",
  components: { JumboComponent, AvadaMessageComponent, LatestNewsComponent, BlackBannerComponent }
}
</script>

<style scoped lang="scss">

</style>
