<template>
    <div id="latestNews">

        <div class="container">

            <div class="title-container d-flex flex-column">

                <div class="title text-center">
                    <h3 class="text-uppercase">Phasellus Eget Metus</h3>
                    <h2>All the latest news</h2>
                </div>

                <div class="orange-separator align-self-center mt-4"></div>

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

            .orange-separator {
                height: 2px;
                width: 5%;
                background-color: $tr-brand-salmon;
            }
        }



    }
}
</style>