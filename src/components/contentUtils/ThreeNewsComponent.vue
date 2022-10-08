<template>

    <div class="three-in-one">

        <div v-for="(article) in articles" :key="article.imgName" class="col-4">

            <img :src="require(`@/assets/images/${article.imgName}`)" alt="img">

            <div class="title fw-bold">{{article.title}}</div>

            <div class="articleInfo d-flex">

                <div class="date">{{article.articleDate}}</div>
                <div class="comments">Comments {{article.articleComments}}</div>

            </div>
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
@import '@/assets/style/variables.scss';

// Contenitore di tre elementi
.three-in-one {
    display: flex;
    justify-content: space-between;
    gap: $tr-gap-10;

    img {
        width: calc(100% - ($tr-gap-10 * 2));
    }

    .articleInfo {

        .date {

            // Barra divisoria tra data e commenti
            &::after {
                content: '|';
                padding: 0 5px;
            }

        }

    }

}
</style>