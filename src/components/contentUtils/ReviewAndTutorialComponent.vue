<template>
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
</template>

<script>
export default {
    name: 'ReviewAndTutorialComponent'
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

}
</style>