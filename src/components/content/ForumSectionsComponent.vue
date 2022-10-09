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

        <div class="forum-cards container d-flex flex-wrap justify-content-between">

            <div v-for="forumInfo in forumInfos" :key="forumInfo.name" class="col-3 p-3">
                <ForumCardComponent :forumInfo="forumInfo" />
            </div>

        </div>


    </div>
</template>

<script>
import ForumCardComponent from '../contentUtils/ForumCardComponent.vue';
export default {
    name: "ForumSectionsComponent",
    data() {
        return {
            forumInfos: [
                {
                    icon: 'fas fa-file-lines',
                    name: 'News & Community'
                },
                {
                    icon: 'fa-brands fa-apple',
                    name: 'Apple Forum'
                },
                {
                    icon: 'fa-brands fa-windows',
                    name: 'Microsoft Forum'
                },
                {
                    icon: 'fa-brands fa-android',
                    name: 'Android Forum'
                },
                {
                    icon: 'fas fa-mug-saucer',
                    name: 'General Discussion'
                },
                {
                    icon: 'fas fa-cubes',
                    name: 'Apps & Software'
                },
                {
                    icon: 'fas fa-laptop',
                    name: 'Gadgets & Stuff'
                },
                {
                    icon: 'fas fa-wrench',
                    name: 'Tutorials & Guides'
                }
            ]
        }
    },
    components: { ForumCardComponent }
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