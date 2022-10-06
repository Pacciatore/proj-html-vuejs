<template>
    <div class="jumbo-container text-white">

        <div class="container">

            <h1>Tech Forum!</h1>
            <p>Discuss all the latest technology news and trends</p>
            <div class="btn-container">
                <button class="btn btn-primary text-uppercase">Get Avada now!
                    <font-awesome-icon icon="fa-solid fa-angle-right" />
                </button>
            </div>

        </div>

    </div>
</template>

<script>
export default {
    name: 'JumboComponent'
}
</script>

<style lang="scss" scoped>
@import '@/assets/style/variables.scss';

.jumbo-container {
    min-height: 200px;

    background-image: url(@/assets/images/home_slider_bg.jpg);

    button {
        border-radius: 0;
        border: none;

        background-color: $tr-brand-color;
    }

}
</style>