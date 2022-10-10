<template>
    <div class="top-footer">

        <div class="container d-flex">

            <div v-for="element in footerElements" :key="element.title">
                <TopFooterElementComponent :element="element" />
            </div>

        </div>
    </div>
</template>

<script>
import TopFooterElementComponent from '../contentUtils/TopFooterElementComponent.vue';
export default {
    name: "TopFooterComponent",
    data() {
        return {
            footerElements: [
                {
                    title: 'Avada Tech Forum',
                    questions: ['Sed semper, nisl id feugiat eleifend, erat est digssim felis, quis auctor elit enim nec ante. Cras et nibh risus. Pellentesque non mi sit amet mi intermentum.']
                },
                {
                    title: 'Popular Topics',
                    questions: ['Sed semper, nisl id feugiat eleifend, erat est digssim felis, quis auctor elit enim nec ante. Cras et nibh risus. Pellentesque non mi sit amet mi intermentum.']
                },
                {
                    title: 'Recent Topics',
                    questions: ['Sed semper, nisl id feugiat eleifend, erat est digssim felis, quis auctor elit enim nec ante. Cras et nibh risus. Pellentesque non mi sit amet mi intermentum.']
                },
                {
                    title: 'Latest Replies',
                    questions: ['Sed semper, nisl id feugiat eleifend, erat est digssim felis, quis auctor elit enim nec ante. Cras et nibh risus. Pellentesque non mi sit amet mi intermentum.']
                }
            ]
        }
    },
    components: { TopFooterElementComponent }
}
</script>

<style lang="scss" scoped>

</style>