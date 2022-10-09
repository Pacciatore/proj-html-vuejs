<template>
    <div class="card p-4 rounded-0 border-0">

        <div class="icon-container text-center p-4">
            <font-awesome-icon class="icon p-4 rounded-circle" :icon="forumInfo.icon" />
        </div>

        <a href="#">{{ forumInfo.name }}</a>

    </div>
</template>

<script>
export default {
    name: 'ForumCardComponent',
    props: {
        forumInfo: Object
    }
}
</script>

<style lang="scss" scoped>
@import '@/assets/style/variables.scss';

.card {

    // Uso di important per sovrascrivere bootstrap rules
    padding-bottom: 75px !important;
    border-top: 5px solid $tr-brand-color !important;

    .icon {
        color: white;
        background-color: $tr-brand-salmon;

        height: 50px;
        width: 50px;
    }

    a {
        color: inherit;
        text-decoration: none;
        text-align: center;

        font-weight: 700;
        font-size: 1.25rem;

    }

}
</style>