<template>
    <div class="px-2">

        <h5>{{ element.title }}</h5>

        <div v-for="(question, index) in element.questions" :key="index">

            <!-- Display site info -->
            <p v-if="element.questions.length === 1" class="info">{{ question }}</p>

            <!-- Display topics -->
            <a v-else href="#" class="question">

                <div class="icon-container">
                    <font-awesome-icon v-if="element.questions.length > 1" icon="fa-solid fa-angle-right" />
                </div>
                <p>{{ question }}</p>

            </a>

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

.px-2 {

    h5 {
        font-weight: 700;
        text-transform: uppercase;

        padding-bottom: 20px;
    }

    .info {
        color: $tr-silver-chalice;
        font-weight: 600;
    }

    .question {
        padding: 10px 0;
        border-bottom: 1px solid $tr-custom-grey;

        color: inherit;
        text-decoration: none;

        display: flex;

        .icon-container {
            padding-right: 10px;
        }

    }
}
</style>