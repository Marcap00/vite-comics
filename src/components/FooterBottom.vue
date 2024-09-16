<script>

export default {
    data() {
        return {
            images: [
                {
                    imageUrl: "facebook",
                    alt: "facebook"
                },
                {
                    imageUrl: "twitter",
                    alt: "twitter"
                },
                {
                    imageUrl: "youtube",
                    alt: "youtube"
                },
                {
                    imageUrl: "pinterest",
                    alt: "pinterest"
                },
                {
                    imageUrl: "periscope",
                    alt: "periscope"
                }
            ]

        }
    },
    methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }

}
</script>

<template>
    <div class="bg-footer-bottom">
        <div class="container">
            <div class="footer-bottom">
                <button type="button">SIGN-UP NOW!</button>
                <div class="social">
                    <h3>FOLLOW US</h3>
                    <img v-for="image in images" :src="getImagePath(`../assets/img/footer-${image.imageUrl}.png`)"
                        :alt="image.alt">
                </div>
            </div>
        </div>
    </div>

</template>

<style lang="scss" scoped>
.bg-footer-bottom {
    background-color: #303030;

    .footer-bottom {
        height: 80px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 3rem 0;


        button {
            background-color: transparent;
            border: 2px solid dodgerblue;
            color: #fff;
            font-weight: 600;
            padding: .5rem;
        }

        .social {
            color: dodgerblue;
            display: flex;
            align-items: center;
            gap: 1rem;
        }
    }
}
</style>