<template>
    <div id="latestNews">

        <div class="container">

            <!-- Contenitore titolo, sottotitolo e separatore -->
            <div class="title-container d-flex flex-column">

                <div class="title text-center">
                    <h3 class="text-uppercase">Phasellus Eget Metus</h3>
                    <h2>All the latest news</h2>
                </div>

                <div class="orange-separator align-self-center mt-4"></div>

            </div>

            <!-- First 3 in 1 -->
            <div class="three-in-one pt-5">

                <div class="col-3">
                    <img src="@/assets/images/post_feat_img_25-320x202.jpg" alt="img">
                </div>

                <div class="col-3">
                    <img src="@/assets/images/post_feat_img_24-320x202.jpg" alt="img">
                </div>

                <div class="col-3">
                    <img src="@/assets/images/post_feat_img_23-320x202.jpg" alt="img">
                </div>

            </div>

            <!-- One big element -->
            <div class="one-in-one">
                <div class="col p-5">

                    <div class="title-container">
                        <h3>Featured Articles</h3>
                        <h2>Cras malesuada et orci eget pharetra</h2>
                    </div>

                </div>
            </div>

            <!-- Second 3 in 1 -->
            <div class="three-in-one">

                <div class="col-3">
                    <img src="@/assets/images/post_feat_img_22-320x202.jpg" alt="img">
                </div>

                <div class="col-3">
                    <img src="@/assets/images/post_feat_img_21-320x202.jpg" alt="img">
                </div>

                <div class="col-3">
                    <img src="@/assets/images/post_feat_img_20-320x202.jpg" alt="img">
                </div>

            </div>

            <!-- One 2/3 and 1/3 -->
            <div class="two-and-one gap-5 pt-5">

                <div class="col-6">
                    <img class="img-fluid" src="@/assets/images/featured_article_2_bg.jpg" alt="featured_2">
                </div>

                <div class="col-3">
                    <div class="title-container">
                        <h2>Tutorial & Guides</h2>
                        <div class="orange-separator one-third"></div>
                    </div>
                </div>

            </div>


        </div>

    </div>
</template>

<script>
export default {
    name: 'LatestNewsComponent'
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

        // Contenitore di tre elementi
        .three-in-one {
            display: flex;
            justify-content: space-between;

        }

        // Contenitore elemento unico
        .one-in-one {

            // Unico elemento
            .col {
                display: flex;
                flex-direction: column-reverse;

                margin-right: 10px;

                height: 670px;

                background-image: url(@/assets/images/featured_article_1_bg.jpg);
                background-size: contain;
            }
        }

        // Contenitore un 2/3 ed un 1/3
        .two-and-one {
            display: flex;
        }

    }
}
</style>