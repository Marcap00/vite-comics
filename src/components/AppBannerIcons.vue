<script>
export default {
    data() {
        return {
            imagesBannerIcons: [
                {
                    url: 'buy-comics-digital-comics.png',
                    text: 'DIGITAL COMICS'
                },
                {
                    url: 'buy-comics-merchandise.png',
                    text: 'DC MERCHANDISE'
                },
                {
                    url: 'buy-comics-subscriptions.png',
                    text: 'SUBSCRIPTIONS'
                },
                {
                    url: 'buy-comics-shop-locator.png',
                    text: 'COMIC SHOP LOCATOR'
                },
                {
                    url: 'buy-dc-power-visa.svg',
                    text: 'DC POWER VISA'
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
    <div class="bg-banner-icons">
        <div class="container">
            <div class="banner-icons">
                <div v-for="image in imagesBannerIcons" class="banner-icon">
                    <img :src="getImagePath(`../assets/img/${image.url}`)" :alt="image.text">
                    <p>{{ image.text }}</p>
                </div>
            </div>
        </div>
    </div>

</template>

<style lang="scss" scoped>
.bg-banner-icons {
    background-color: dodgerblue;

    .banner-icons {
        display: flex;
        justify-content: space-evenly;
        padding: 3rem 0;

        .banner-icon {
            display: flex;
            align-items: center;
            gap: .5rem;
            color: white;
            font-weight: 600;

            img {
                max-width: 50px;
                height: 50px;
            }
        }
    }
}

@media screen and (max-width: 1080px) {

    .banner-icon {
        img {
            max-width: 40px;
            height: 40px;
        }

        p {
            font-size: 14px;
        }
    }
}

@media screen and (max-width: 1080px) {

    .banner-icon {

        p {
            margin-right: 20px;
        }
    }
}
</style>