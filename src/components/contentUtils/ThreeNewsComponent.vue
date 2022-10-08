<template>

    <div class="three-in-one">

        <div v-for="(article) in articles" :key="article.imgName" class="col-3">

            <img :src="require(`@/assets/images/${article.imgName}`)" alt="img">
            <div class="date">{{article.articleDate}}</div>
            <div class="comments">Comments {{article.articleComments}}</div>
            <div class="incipit-text">{{article.incipitText}}</div>

        </div>

    </div>

</template>

<script>
export default {
    name: 'ThreeNewsComponent',
    props: {
        articles: Array
    }

}
</script>

<style lang="scss" scoped>
// Contenitore di tre elementi
.three-in-one {
    display: flex;
    justify-content: space-between;

}
</style>