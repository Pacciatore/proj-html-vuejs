<template>
    <div class="top-footer">

        <div class="container d-flex">

            <div v-for="element in footerElements" :key="element.title" class="col-3">
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
                    questions: [
                        'Sed semper, nisl id feugiat eleifend, erat est digssim felis, quis auctor elit enim nec ante. Cras et nibh risus. Pellentesque non mi sit amet mi intermentum.'
                    ]
                },
                {
                    title: 'Popular Topics',
                    questions: [
                        'Nam a dolor volutpat massa auctor semper',
                        'Sed euismod nunc urna fermentum arcu dapibus fringilla.',
                        'Cras lacinia tellus id mauris finibus lacus molestie',
                        'Curabitur a scelerisque ligula'
                    ]
                },
                {
                    title: 'Recent Topics',
                    questions: [
                        'Cras lacinia tellus id mauris finibus lacus molestie',
                        'Proin at ligula sagittis vestibulum nisi vitae',
                        'Sed nec metus at est tincidunt elementum',
                        'Nulla egestas nulla eu nulla sucipit molestie'
                    ]
                },
                {
                    title: 'Latest Replies',
                    questions: [
                        'Cras lacinia tellus id mauris finibus lacus molestie',
                        'Cras lacinia tellus id mauris finibus lacus molestie',
                        'Nulla egestas nulla eu nulla sucipit molestie',
                        'Mauris ac nibh quis eros sagittis lacinia a et dui'
                    ]
                }
            ]
        }
    },
    components: { TopFooterElementComponent }
}
</script>

<style lang="scss" scoped>

</style>