<template>
    <div class="avada-message">

        <div class="container text-center">
            <h5 class="text-uppercase fw-semibold">Avada Forum is the place to be</h5>
            <p>In quis lectus sed leo elementum faucibus in dapibus dictum.</p>
            <p> Nulla molestie tortor nec lectus, venenatis, sed blandit dui finibus.</p>
            <p> dolor at, bibendum purus. Donec vehicula nec tortor ac finibus.</p>
        </div>

    </div>
</template>

<script>
export default {
    name: 'AvadaMessageComponent'
}
</script>

<style lang="scss" scoped>
@import '@/assets/style/variables.scss';

.avada-message {
    background-color: $tr-custom-grey;

    padding: $tr-py-100;

    h5 {
        color: $tr-cape-cod;
        font-size: $tr-fs-07;
        letter-spacing: $tr-title-ls;
        margin-bottom: 1rem;
    }

    p {
        font-weight: 300;
        color: $tr-nevada;
        margin: 0;
    }

}
</style>