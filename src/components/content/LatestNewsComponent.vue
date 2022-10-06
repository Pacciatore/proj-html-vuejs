<template>
    <div id="latestNews">

        <div class="container">

            <div class="title text-center">
                <h3 class="text-uppercase">Phasellus Eget Metus</h3>
                <h2>All the latest news</h2>
            </div>

            <div class="orange-separator"></div>

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

        .title {
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
        }

    }
}
</style>