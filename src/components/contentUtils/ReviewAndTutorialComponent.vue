<template>
    <div class="two-and-one pt-5">

        <!-- Reviewed article: sostanzialmente one-in-one ma più piccolo -->
        <div class="col-8 reviewed-article">
            <div class="content">

                <div class="title-container">
                    <h3>Reviewed Product</h3>
                    <h2>Mauris viverra atisn ipsum eget felis prims efficitur varius</h2>
                </div>

                <p>In quis lectus sed leo elementum faucibus in dapibus dictum. Nullamolestie tortor nec lectus
                    venenatis, sed blandit dui, dolor at bibendum.
                </p>

                <div class="btn-container">
                    <button class="btn btn-dark rounded-0 text-uppercase px-5 py-3 fs-4 fw-semibold">Read More
                        <font-awesome-icon class="ps-2" icon="fa-solid fa-angle-right" />
                    </button>
                </div>

            </div>
        </div>

        <!-- Tutorials & Guides -->
        <div class="col-4 tutorial-guides">

            <div class="title-container">
                <h2>Tutorial & Guides</h2>
                <div class="orange-separator one-third my-4"></div>
            </div>

            <div class="articles-container col py-2">

                <div class="article" v-for="tutorial in tutorials" :key="tutorial.title">

                    <div class="img-container col-4">
                        <img :src="require(`@/assets/images/${tutorial.imgName}`)" alt="img">
                    </div>

                    <div class="articleInfo col d-flex flex-column pt-1 ps-5">

                        <div class="title text-black fw-bold fs-5">{{ tutorial.title }}</div>

                        <!-- Data e Commenti -->
                        <div class="col d-flex pt-1">
                            <div class="date">{{tutorial.date}}</div>
                            <div class="comments" :class="{ off : tutorial.comments === 'Off'}">
                                <span>Comments</span>
                                <span>{{tutorial.comments}}</span>
                            </div>
                        </div>

                    </div>


                </div>

            </div>

        </div>

    </div>
</template>

<script>
export default {
    name: 'ReviewAndTutorialComponent',
    props: {
        tutorials: Array
    }
}
</script>

<style lang="scss" scoped>
@import '@/assets/style/variables.scss';

.two-and-one {
    display: flex;

    .title-container {

        // h3 and h2 classes
        h3 {
            color: $tr-cape-cod;
            font-size: $tr-fs-07;
            letter-spacing: $tr-title-ls;
            margin-bottom: 1rem;
            font-weight: 700;
        }

        h2 {
            font-weight: 700;
        }

        .orange-separator {
            height: 2px;
            width: 5%;
            background-color: $tr-brand-salmon;

            // Classe speciale per l'orange separator nell'1/3
            &.one-third {
                width: 30%;
            }

        }
    }

    // 2/3 element
    // TODO: è sostanzialmente il one-in-one di LatestNews
    .reviewed-article {

        padding-right: calc($tr-gap-30 / 2);

        color: white;

        .content {
            display: flex;
            flex-direction: column;
            justify-content: flex-end;

            padding: 100px;
            padding-top: 150px;

            background-image: url(@/assets/images/featured_article_2_bg.jpg);
            background-size: cover;

            line-height: 2rem;

            h3 {
                color: inherit;
                text-transform: uppercase;
                font-size: 1.25rem;
                padding-bottom: 5px;
            }

            h2 {
                font-size: 2.75rem;
            }

            p {
                padding: 20px 0;
            }

        }

    }

    // 1/3 element
    .tutorial-guides {

        display: flex;
        flex-direction: column;

        padding-left: $tr-gap-30;

        // Contenitore tutorial e guide thumbs
        .articles-container {
            display: flex;
            flex-direction: column;
            justify-content: space-between;

            .article {
                display: flex;
                // flex-direction: column;
                flex-wrap: wrap;

                // Info: Titolo, Data e Commenti
                .articleInfo {

                    font-size: .85rem;

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

        }

    }

}
</style>