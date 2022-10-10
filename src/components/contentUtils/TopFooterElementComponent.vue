<template>
    <div>

        <h6>{{ element.title }}</h6>

        <div v-for="(question, index) in element.questions" :key="index">
            {{ question }}
        </div>

    </div>
</template>

<script>
export default {
    name: 'TopFooterElementComponent',
    props: {
        element: Object
    }
}
</script>

<style lang="scss" scoped>

</style>