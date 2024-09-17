<script>
import CardsItem from './ListCardsItem.vue';

export default {
    data() {
        return {

        }
    },
    components: {
        CardsItem
    }
}
</script>

<template>
    <div class="bg-main">
        <div class="container">
            <h3>CURRENT SERIES</h3>
            <div class="list-cards">

                <CardsItem />

            </div>
            <button type="button">LOAD MORE</button>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.bg-main {
    background-color: #1C1C1C;

    .container {
        text-align: center;
        position: relative;
        padding-top: 2rem;
    }


    h3,
    button {
        color: white;
        background-color: dodgerblue;
    }

    h3 {
        display: inline-block;
        padding: .5rem 1rem;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
        position: absolute;
        top: -20px;
        left: 0;
    }

    button {
        font-weight: 700;
        border: 1px solid dodgerblue;
        padding: .5rem 2.5rem;
        margin: 1rem 0;
        cursor: pointer;
    }
}
</style>