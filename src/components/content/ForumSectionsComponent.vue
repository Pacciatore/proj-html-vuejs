<template>
    <div id="forum-sections" class="py-5">

        <!-- Contenitore titolo, sottotitolo e separatore -->
        <div class="title-container d-flex flex-column pb-5">

            <div class="title text-center">
                <h3 class="text-uppercase">Phasellus Eget Metus</h3>
                <h2>Forum Sections</h2>
            </div>

            <div class="orange-separator align-self-center mt-4"></div>

        </div>



    </div>
</template>

<script>
export default {
    name: 'ForumSectionsComponent'
}
</script>

<style lang="scss" scoped>
@import '@/assets/style/variables.scss';

#forum-sections {
    background-color: $tr-custom-grey;

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