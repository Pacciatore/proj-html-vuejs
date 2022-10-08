<template>
    <div id="latestNews">

        <div class="container">

            <!-- Contenitore titolo, sottotitolo e separatore -->
            <div class="title-container d-flex flex-column pb-5">

                <div class="title text-center">
                    <h3 class="text-uppercase">Phasellus Eget Metus</h3>
                    <h2>All the latest news</h2>
                </div>

                <div class="orange-separator align-self-center mt-4"></div>

            </div>

            <!-- First 3 in 1 -->
            <ThreeNewsComponent :articles="latestNews.slice(0,3)" />

            <!-- One big element -->
            <div class="one-in-one my-5">
                <div class="col">

                    <div class="title-container">
                        <h3>Featured Articles</h3>
                        <h2>Cras malesuada et orci eget pharetra</h2>
                    </div>

                    <p>In quis lectus sed leo elementum faucibus in dapibus dictum. Nullamolestie tortor nec lectus
                        venenatis, sed blandit dui, dolor at bibendum sadips ets ipsums dolores ficilis uns leo lectus.
                    </p>

                    <div class="btn-container">
                        <button class="btn btn-dark rounded-0 text-uppercase px-4 py-2 fw-semibold">Read More
                            <font-awesome-icon class="ps-2" icon="fa-solid fa-angle-right" />
                        </button>
                    </div>

                </div>
            </div>

            <!-- Second 3 in 1 -->
            <ThreeNewsComponent class="pt-2" :articles="latestNews.slice(3,6)" />

            <!-- One 2/3 and 1/3 -->
            <ReviewAndTutorialComponent :tutorials="tutorials" />

        </div>

    </div>
</template>

<script>
import ThreeNewsComponent from "../contentUtils/ThreeNewsComponent.vue";
import ReviewAndTutorialComponent from "../contentUtils/ReviewAndTutorialComponent.vue";
export default {
    name: "LatestNewsComponent",
    components: { ThreeNewsComponent, ReviewAndTutorialComponent },
    data() {
        return {
            latestNews: [
                {
                    title: 'Morbi vitae dui euismod vulputate sollicitudin',
                    imgName: `post_feat_img_25-320x202.jpg`,
                    articleDate: 'October 11th, 2015',
                    articleComments: '2',
                    incipitText: `Donnec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fingilla, vestibulum placerat metus mattis. Aenean dictum viate nisl`
                },
                {
                    title: 'Vivamus pellenteque, fellis quis varius',
                    imgName: `post_feat_img_24-320x202.jpg`,
                    articleDate: 'October 11th, 2015',
                    articleComments: 'Off',
                    incipitText: `Donnec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fingilla, vestibulum placerat metus mattis. Aenean dictum viate nisl`
                },
                {
                    title: 'Donnec ornare pretium scelisque justo',
                    imgName: `post_feat_img_23-320x202.jpg`,
                    articleDate: 'October 11th, 2015',
                    articleComments: 'Off',
                    incipitText: `Donnec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fingilla, vestibulum placerat metus mattis. Aenean dictum viate nisl`
                },
                {
                    title: 'Fusce sollicitudin nunc sed placerat varius',
                    imgName: `post_feat_img_22-320x202.jpg`,
                    articleDate: 'October 11th, 2015',
                    articleComments: 'Off',
                    incipitText: `Donnec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fingilla, vestibulum placerat metus mattis. Aenean dictum viate nisl`
                },
                {
                    title: 'Donec facilis sodales leo sit amet laoreet',
                    imgName: `post_feat_img_21-320x202.jpg`,
                    articleDate: 'October 11th, 2015',
                    articleComments: 'Off',
                    incipitText: `Donnec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fingilla, vestibulum placerat metus mattis. Aenean dictum viate nisl`
                },
                {
                    title: 'Proin eu purus sed aru aliquet curabir vens',
                    imgName: `post_feat_img_20-320x202.jpg`,
                    articleDate: 'October 11th, 2015',
                    articleComments: 'Off',
                    incipitText: `Donnec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fingilla, vestibulum placerat metus mattis. Aenean dictum viate nisl`
                }
            ],
            tutorials: [
                {
                    title: 'Donec ornare pretium eget scelisque justo',
                    date: 'October 11th, 2015',
                    comments: 'Off'
                },
                {
                    title: 'Fusce sollicitudin nunc sed placerat varius',
                    date: 'October 11th, 2015',
                    comments: 'Off'
                },
                {
                    title: 'Proin eu purus sed aru aliquet curabir vens',
                    date: 'October 11th, 2015',
                    comments: 'Off'
                }
            ]

        }
    }
}
</script>

<style lang="scss" scoped>
@import '@/assets/style/variables.scss';

#latestNews {
    .container {
        padding: $tr-py-100;

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

        // Contenitore elemento unico
        .one-in-one {

            color: white;

            // Unico elemento
            .col {
                display: flex;
                flex-direction: column;
                justify-content: flex-end;

                padding: 100px;
                padding-top: 300px;


                background-image: url(@/assets/images/featured_article_1_bg.jpg);
                background-size: cover;

                h3 {
                    color: inherit;
                    text-transform: uppercase;
                    font-size: .9rem;
                }

                h2 {
                    font-size: 3rem;
                }

                p {
                    padding: 20px 0;
                }

            }
        }

    }
}
</style>