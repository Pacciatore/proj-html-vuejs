<template>
    <div class="py-5">
        <div class="container d-flex justify-content-between">

            <!-- Colonna delle note legali -->
            <div class="legal-notes col-6 d-flex">

                <div class="col">Copyright</div>
                <div class="col">Avada</div>
                <div class="col">All Rights</div>
                <div class="col">Powered by</div>

            </div>

            <!-- Colonna per i link social -->
            <div class="social-links col-3 d-flex justify-content-end">

                <font-awesome-icon icon="fa-brands fa-facebook-f" />
                <font-awesome-icon icon="fa-brands fa-twitter" />
                <font-awesome-icon icon="fa-brands fa-instagram" />
                <font-awesome-icon icon="fa-brands fa-youtube" />

            </div>

        </div>
    </div>
</template>

<script>
export default {
    name: 'BottomFooterComponent'
}
</script>

<style lang="scss" scoped>
@import '@/assets/style/variables.scss';

div.py-5 {
    border-top: 1px solid $tr-custom-grey;
}
</style>