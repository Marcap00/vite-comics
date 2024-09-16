<script>
export default {
    data() {
        return {
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
    }
}
</script>

<template>
    <header>
        <img src="../assets/img/dc-logo.png" alt="Logo DC Comics">
        <nav>
            <ul>
                <li v-for="link in navbarLinks">
                    <a :href="link.href"> {{ link.text }} </a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style scoped>

</style>