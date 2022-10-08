<template>

    <div class="three-in-one">

        <div v-for="(article) in articles" :key="article.imgName" class="col">

            <img :src="require(`@/assets/images/${article.imgName}`)" alt="img">

            <div class="title text-black fw-bold">{{article.title}}</div>

            <div class="articleInfo d-flex">

                <div class="date">{{article.articleDate}}</div>
                <div class="comments" :class="{ off : article.articleComments === 'Off'}">
                    <span>Comments</span>
                    <span>{{article.articleComments}}</span>
                </div>

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
    gap: $tr-gap-30;

    color: $tr-nevada;

    img {
        width: 100%;
    }

    .articleInfo {

        .date {

            // Barra divisoria tra data e commenti
            &::after {
                content: '|';
                padding: 0 5px;
            }

        }

        .comments {
            color: black;
            display: flex;
            flex-direction: row-reverse;

            font-weight: 600;

            :nth-child(2) {
                padding-right: 5px;
            }

            &.off {
                color: inherit;
                flex-direction: row;

                font-weight: inherit;

                :nth-child(1) {
                    padding-right: 5px;
                }

            }
        }

    }

}
</style>