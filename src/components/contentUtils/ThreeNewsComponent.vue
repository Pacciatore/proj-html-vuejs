<template>
    <!-- First 3 in 1 -->
    <div class="three-in-one">

        <div class="col-3">
            <img src="@/assets/images/post_feat_img_25-320x202.jpg" alt="img">
        </div>

        <div class="col-3">
            <img src="@/assets/images/post_feat_img_24-320x202.jpg" alt="img">
        </div>

        <div class="col-3">
            <img src="@/assets/images/post_feat_img_23-320x202.jpg" alt="img">
        </div>

    </div>

</template>

<script>
export default {
    name: 'ThreeNewsComponent'
}
</script>

<style lang="scss" scoped>
// Contenitore di tre elementi
.three-in-one {
    display: flex;
    justify-content: space-between;

}
</style>