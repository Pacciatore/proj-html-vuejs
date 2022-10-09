<template>
  <main>

    <JumboComponent />
    <AvadaMessageComponent />
    <LatestNewsComponent />
    <BlackBannerComponent :text="'Read our blog'" />
    <ForumSectionsComponent />
    <BlackBannerComponent :text="'Go to our forum'" />


  </main>
</template>

<script>
import JumboComponent from './content/JumboComponent.vue';
import AvadaMessageComponent from './content/AvadaMessageComponent.vue';
import LatestNewsComponent from './content/LatestNewsComponent.vue';
import BlackBannerComponent from './contentUtils/BlackBannerComponent.vue';
import ForumSectionsComponent from './content/ForumSectionsComponent.vue';
export default {
  name: "MainComponent",
  components: { JumboComponent, AvadaMessageComponent, LatestNewsComponent, BlackBannerComponent, ForumSectionsComponent }
}
</script>

<style scoped lang="scss">

</style>
