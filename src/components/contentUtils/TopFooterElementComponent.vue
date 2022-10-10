<template>
    <div class="px-2">

        <h5>{{ element.title }}</h5>

        <div v-for="(question, index) in element.questions" :key="index"
            :class="element.questions.length === 1 ? 'info' : 'question' ">
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
@import '@/assets/style/variables.scss';

h5 {
    font-weight: 700;
    text-transform: uppercase;
}

.info {
    color: $tr-silver-chalice;
    font-weight: 600;
}
</style>