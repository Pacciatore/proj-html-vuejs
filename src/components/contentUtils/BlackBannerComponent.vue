<template>
    <div class="py-5">
        <a href="#">
            {{ text }}
            <font-awesome-icon class="ps-2" icon="fa-solid fa-right-long" />
        </a>
    </div>
</template>

<script>
export default {
    name: 'BlackBannerComponent',
    props: {
        text: String
    }
}
</script>

<style lang="scss" scoped>
@import '@/assets/style/variables.scss';

div {
    background-color: $tr-shark;
    color: white;

    text-align: center;
    text-transform: uppercase;
    font-weight: 600;

    a {
        color: inherit;
        text-decoration: none;
    }

}
</style>