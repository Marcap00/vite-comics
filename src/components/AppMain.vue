<script>
import MainHero from './MainHero.vue';
import MainCards from './MainCards.vue';

export default {
    data() {
        return {

        }
    },
    components: {
        MainHero,
        MainCards
    }
}
</script>

<template>
    <main>
        <MainHero />
        <MainCards />
    </main>
</template>

<style lang="scss" scoped></style>