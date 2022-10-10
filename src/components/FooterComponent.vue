<template>
    <footer>

        <TopFooterComponent />
        <BottomFooterComponent />

    </footer>
</template>

<script>
import TopFooterComponent from './content/TopFooterComponent.vue';
import BottomFooterComponent from './content/BottomFooterComponent.vue';
export default {
    name: "FooterComponent",
    components: { TopFooterComponent, BottomFooterComponent }
}
</script>

<style lang="scss" scoped>

</style>