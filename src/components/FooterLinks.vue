<script>
export default {
    data() {
        return {
            footerLists: [
                {
                    title: 'DC COMICS',
                    links: [
                        { href: '#', text: 'Characters', },
                        { href: '#', text: 'Comics', },
                        { href: '#', text: 'Movies', },
                        { href: '#', text: 'TV', },
                        { href: '#', text: 'Games', },
                        { href: '#', text: 'Videos', },
                        { href: '#', text: 'News', }
                    ]
                },
                {
                    title: 'SHOP',
                    links: [
                        { href: '#', text: 'Shop DC', },
                        { href: '#', text: 'Shop DC Collectibles', },

                    ]
                },
                {
                    title: 'DC',
                    links: [
                        { href: '#', text: 'Term Of Use', },
                        { href: '#', text: 'Privacy Policy (New)', },
                        { href: '#', text: 'Ad Choices', },
                        { href: '#', text: 'Advertising', },
                        { href: '#', text: 'Jobs', },
                        { href: '#', text: 'Subsciptions', },
                        { href: '#', text: 'Talent Workshops', },
                        { href: '#', text: 'CPSC Certification', },
                        { href: '#', text: 'Ratings', },
                        { href: '#', text: 'Shop Help', },
                        { href: '#', text: 'Contact Us', }
                    ]
                },
                {
                    title: 'SITES',
                    links: [
                        { href: '#', text: 'DC', },
                        { href: '#', text: 'MAD Magazine', },
                        { href: '#', text: 'DC Kids', },
                        { href: '#', text: 'DC Universe', },
                        { href: '#', text: 'DC Power Visa', }
                    ]
                },
            ]

        }
    }
}
</script>

<template>
    <div class="bg-image">
        <img src="../assets/img/dc-logo-bg.png" alt="">
        <div class="container">
            <div class="wrapper-lists">
                <ul v-for="(list, index) in footerLists">
                    <li class="title">
                        {{ list.title.toUpperCase() }}
                    </li>
                    <li v-for="link in footerLists[index].links">
                        <a :href="link.href"> {{ link.text }} </a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.bg-image {
    background-image: url('../assets/img/footer-bg.jpg');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    position: relative;
    z-index: -1;
    padding: 3rem 0;

    img {
        position: absolute;
        top: -15%;
        right: 30px;

        max-height: 600px;
    }

    .wrapper-lists {
        max-width: 60%;
        height: 350px;
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;

        ul {

            flex-shrink: 1;
            width: 200px;

            li.title {
                color: #fff;
                font-weight: 600;
                font-size: 1.5em;
                margin: 1rem 0;
            }

            li {
                margin: .3rem 0;

                a {
                    color: #6b6b6b;
                }

                a:hover {
                    text-decoration: underline;
                }
            }
        }
    }
}
</style>