<template>
    <header>

        <nav class="container navbar text-white">

            <!-- Logo brand -->
            <div class="navbar-brand">
                <a href="#">
                    <img class="img-fluid" src="@/assets/images/logo.png" alt="avada-logo">
                </a>
            </div>

            <!-- Elenco degli elementi della nav -->
            <ul class="navbar-nav col-7 flex-row justify-content-between">

                <li class="nav-item">
                    <a class="nav-link active" href="#">Home</a>
                    <!-- TODO
                            Triangolo dinamico con la classe active -->
                    <div class="triangle-down"></div>
                </li>

                <li class="nav-item"><a class="nav-link" href="#">Apple</a></li>
                <li class="nav-item"><a class="nav-link" href="#">Microsoft</a></li>
                <li class="nav-item"><a class="nav-link" href="#">Android</a></li>
                <li class="nav-item"><a class="nav-link" href="#">Forums</a></li>
                <li class="nav-item"><a class="nav-link" href="#">Contact us</a></li>
                <li class="nav-item"><button class="text-uppercase fw-semibold btn btn-dark px-4">Join us</button></li>
                <li class="nav-item d-flex align-items-center">
                    <font-awesome-icon icon="fa-solid fa-magnifying-glass" />
                </li>

            </ul>

        </nav>

    </header>
</template>

<script>
export default {
    name: 'HeaderComponent'
}
</script>

<style lang="scss" scoped>
@import '@/assets/style/variables.scss';

header {
    background-color: $tr-header-bg;

    .nav-item {

        position: relative;

        .triangle-down {
            position: absolute;
            top: 55px;
            width: 0;
            height: 0;
            border-left: 20px solid transparent;
            border-right: 20px solid transparent;

            border-top: 20px solid $tr-header-bg;
        }

        .nav-link {
            color: inherit;

            font-weight: 300;

            &.active {
                color: inherit;
            }

        }

        button {
            border-radius: 0;
        }
    }

}
</style>