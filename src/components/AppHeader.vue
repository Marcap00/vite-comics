<script>
export default {
    data() {
        return {
            currentIndex: 0,
            navbarLinks: [
                {active: true, href: '#', text: 'Characters',},
                {active: false, href: '#', text: 'Comics',},
                {active: false, href: '#', text: 'Movies',},
                {active: false, href: '#', text: 'TV',},
                {active: false, href: '#', text: 'Games',},
                {active: false, href: '#', text: 'Collectibles',},
                {active: false, href: '#', text: 'Videos',},
                {active: false, href: '#', text: 'News',},
                {active: false, href: '#', text: 'Shop',}
            ]
        }
    },
    methods: {
        setActiveLink(index) {
            this.navbarLinks.forEach((link, i) => {
                /* link.active = i === index ? true : false; */
                link.active = i === index;
            });
        }
    }
}
</script>

<template>
    <header class="container">
        <img src="../assets/img/dc-logo.png" alt="Logo DC Comics">
        <nav>
            <ul>
                <li v-for="(link, index) in navbarLinks">
                    <a @click="setActiveLink(index)" :class="{ active: link.active }" :href="link.href"> {{ link.text.toUpperCase() }} </a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
header {
    height: 100px;
    padding: 10px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    
    ul {
        display:flex;
        gap: 1.5rem;

        a {
            display: inline-block;
            line-height: 100px;
            color: black;
            font-weight: 600;
            &.active, &:hover {
                color: dodgerblue;
                border-bottom: 4px solid currentColor;
            }
        }
    }
}

</style>