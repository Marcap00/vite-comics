<script>
import MainHero from './MainHero.vue';
import MainListCards from './MainListCards.vue';

export default {
    data() {
        return {

        }
    },
    components: {
        MainHero,
        MainListCards
    }
}
</script>

<template>
    <main>
        <MainHero />
        <MainListCards />
    </main>
</template>

<style lang="scss" scoped></style>