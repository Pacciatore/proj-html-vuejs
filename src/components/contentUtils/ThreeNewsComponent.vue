<template>

    <div class="three-in-one">

        <div v-for="(image, index) in images" :key="index" class="col-3">
            <img :src="require(`@/assets/images/${image}`)" alt="img">
        </div>

    </div>

</template>

<script>
export default {
    name: 'ThreeNewsComponent',
    data() {
        return {
            imgName: 'post_feat_img_',
            imgDimension: '320x202',
            images: []
        }
    },
    props: {
        imgNums: Array
    },
    created() {
        this.imgUrlMaker()
    },
    methods: {
        imgUrlMaker() {

            for (let i = 0; i < 3; i++) {
                const imgUrl = `${this.imgName}${this.imgNums[i]}-${this.imgDimension}.jpg`;
                this.images.push(imgUrl)
            }

        }
    }
}
</script>

<style lang="scss" scoped>
// Contenitore di tre elementi
.three-in-one {
    display: flex;
    justify-content: space-between;

}
</style>