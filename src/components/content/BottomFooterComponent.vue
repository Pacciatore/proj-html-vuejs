<template>
    <div class="py-5">
        <div class="container d-flex justify-content-between">

            <!-- Colonna delle note legali -->
            <div class="legal-notes col-6">

                <span>&copy; Copyright 2012 - 2020</span>
                <span>Avada Theme by <a href="#">Theme Fusion</a></span>
                <span>All Rights Reserved</span>
                <span>Powered by <a href="#">WordPress</a></span>

            </div>

            <!-- Colonna per i link social -->
            <div class="social-links col-2 d-flex justify-content-between">

                <div class="icon-container rounded-circle fb">
                    <a href="#">
                        <font-awesome-icon icon="fa-brands fa-facebook-f" />
                    </a>
                </div>

                <div class="icon-container rounded-circle tw">
                    <a href="#">
                        <font-awesome-icon icon="fa-brands fa-twitter" />
                    </a>
                </div>

                <div class="icon-container rounded-circle insta">
                    <a href="#">
                        <font-awesome-icon icon="fa-brands fa-instagram" />
                    </a>
                </div>

                <div class="icon-container rounded-circle yt">
                    <a href="#">
                        <font-awesome-icon icon="fa-brands fa-youtube" />
                    </a>
                </div>

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

    font-size: .85rem;

    .legal-notes {
        color: $tr-silver-chalice;
        font-weight: 600;

        display: flex;
        align-items: center;

        // Barra divisoria elementi interni
        :not(:first-child):before {
            content: '|';
            font-weight: 500;
            padding: 0 5px;
        }

        a {
            color: $tr-shark;
            text-decoration: none;
        }

    }

    .social-links {
        color: white;

        .icon-container {

            padding: 10px;

            * {
                color: inherit;
                // Perché prendono la forma di m&m's?
                height: 1.5rem;
                width: 1.5rem;
            }

            &.fb {
                background-color: $tr-facebook-blue;
            }

            &.tw {
                background-color: $tr-twitter-blue;
            }

            &.insta {
                background-color: $tr-instagram-indaco;
            }

            &.yt {
                background-color: $tr-youtube-red;
            }
        }

    }

}
</style>