<template>
    <header>

        <nav class="container navbar text-white">

            <div class="navbar-brand">
                <img src="@/assets/images/logo.png" alt="avada-logo">
            </div>

            <ul class="navbar-nav w-50 flex-row justify-content-between">

                <li class="nav-item"><a class="nav-link" href="#">Home</a></li>
                <li class="nav-item"><a class="nav-link" href="#">Apple</a></li>
                <li class="nav-item"><a class="nav-link" href="#">Microsoft</a></li>
                <li class="nav-item"><a class="nav-link" href="#">Android</a></li>
                <li class="nav-item"><a class="nav-link" href="#">Forums</a></li>
                <li class="nav-item"><a class="nav-link" href="#">Contact us</a></li>
                <li class="nav-item"><button class="text-uppercase btn btn-dark">Join us</button></li>
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

    .nav-link {
        color: inherit;
    }

}
</style>