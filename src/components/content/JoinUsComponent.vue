<template>
    <!-- TODO:è come il jumbo, cambia il contenuto degli elementi e dello stile -->

    <div class="join-us-container text-white">

        <div class="container text-center w-50">

            <h1>Hey! Join to our Community</h1>
            <p class="py-3 fw-light">Nulla molestie tortor nec lectus venenatis, de blandit dui fiibus. Curabitur
                feugiat vulputate purus ipsums dolores ficilis uns etra.</p>
            <div class="btn-container">
                <button class="btn btn-primary text-uppercase px-4 fw-semibold">Sign Up
                    <font-awesome-icon class="ps-2" icon="fa-solid fa-angle-right" />
                </button>
            </div>

        </div>

    </div>
</template>

<script>
export default {
    name: 'JoinUsComponent'
}
</script>

<style lang="scss" scoped>
@import '@/assets/style/variables.scss';

.join-us-container {
    background-image: url(@/assets/images/join_now_cta_bg.jpg);
    background-size: cover;
    // Aggiunto rispetto al jumbo
    background-position: center;

    padding: $tr-py-100;

    .container {

        h1 {
            // Aggiunto rispetto al jumbo
            width: 75%;
            margin: auto;

            // Modificato rispetto al jumbo
            font-size: 4rem;
            font-weight: 700;
        }

        // Aggiunto rispetto al jumbo
        p {
            width: 65%;
            margin: auto;
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
}
</style>