<template>
    <div class="card p-4">

        <font-awesome-icon :icon="forumInfo.icon" />

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
.card {

    a {
        color: inherit;
        text-decoration: none;
    }

}
</style>