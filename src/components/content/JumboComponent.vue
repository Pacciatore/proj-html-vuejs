<template>
    <div class="jumbo-container text-white">

        <div class="container">

            <h1>Tech Forum!</h1>
            <p class="py-3 fw-light">Discuss all the latest technology news and trends</p>
            <div class="btn-container">
                <button class="btn btn-primary text-uppercase px-4 fw-semibold">Get Avada now!
                    <font-awesome-icon class="ps-2" icon="fa-solid fa-angle-right" />
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
    background-image: url(@/assets/images/home_slider_bg.jpg);
    background-size: cover;

    padding: 310px;

    h1 {
        font-size: 6rem;
        font-weight: 700;
    }

    button {
        border-radius: 0;
        border: none;

        background-color: $tr-brand-color;

        &:hover {
            background-color: $tr-brand-color-hover;
        }
    }

}
</style>