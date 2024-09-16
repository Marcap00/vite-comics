<script>
import FooterLinks from './FooterLinks.vue';
import FooterBottom from './FooterBottom.vue';
export default {
    data() {
        return {

        }
    },
    components: {
        FooterLinks,
        FooterBottom
    }
}
</script>

<template>
    <footer>
        <FooterLinks/>
        <FooterBottom/>
    </footer>
</template>

<style scoped>
footer {
    background-color: #303030;
}

</style>