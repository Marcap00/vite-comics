<script>
import CardsItem from './ListCardsItem.vue';

export default {
    data() {
        return {
            comicsCards: [
                {
                    thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    price: "$19.99",
                    series: "Action Comics",
                    type: "comic book"
                },
                {
                    thumb: "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    price: "$3.99",
                    series: "American Vampire 1976",
                    type: "comic book"
                },
                {
                    thumb: "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    price: "$16.99",
                    series: "Aquaman",
                    type: "graphic novel"
                },
                {
                    thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    price: "$2.99",
                    series: "Batgirl",
                    type: "comic book"
                },
                {
                    thumb: "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    price: "$3.99",
                    series: "Batman",
                    type: "comic book"
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    price: "$2.99",
                    series: "Batman Beyond",
                    type: "comic book"
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    price: "$3.99",
                    series: "Batman/Superman",
                    type: "comic book"
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    price: "$4.99",
                    series: "Batman/Superman Annual",
                    type: "comic book"
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    price: "$5.99",
                    series: "Batman: The Joker War Zone",
                    type: "comic book"
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    price: "$6.99",
                    series: "Batman: Three Jokers",
                    type: "comic book"
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    price: "$4.99",
                    series: "Batman: White Knight Presents: Harley Quinn",
                    type: "comic book"
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    price: "$16.99",
                    series: "Catwoman",
                    type: "graphic novel"
                }
            ]

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
            <div class="list-cards">
                <h3>CURRENT SERIES</h3>
                <div class="row row-cols">

                    <CardsItem v-for="(comicCard, index) in comicsCards" :key="index" :thumbUrl="comicCard.thumb"
                        :price="comicCard.price" :titleSeries="comicCard.series" :type="comicCard.type" />

                </div>
                <button type="button">LOAD MORE</button>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.container {
    text-align: center;
    position: relative;
    padding-top: 2rem;
    padding: 3rem 15px 0 15px;
}

.bg-main {
    background-color: #1C1C1C;



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

@media screen and (max-width: 1080px) {

    .row.row-cols>* {
        flex-basis: 25%;
    }
}
</style>