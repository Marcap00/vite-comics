<script>
export default {
    data() {
        return {

        }
    },
    props: {
        thumbUrl: {
            type: String,
            required: true
        },
        price: {
            type: String,
            required: false
        },
        titleSeries: {
            type: String,
            required: true
        },
        type: {
            type: String,
            required: false
        }
    }
}
</script>

<template>

    <div class="col">
        <div class="card">

            <div class="card-img">
                <img class="card-img" :src="thumbUrl" :alt="titleSeries">
            </div>

            <div class="card-body">
                <h5 class="card-title">
                    {{ titleSeries.toUpperCase() }}
                </h5>
            </div>

        </div>
    </div>
</template>

<style lang="scss" scoped>
.card-img {
    max-height: 150px;
    width: 150px;
    object-fit: cover;
    object-position: top;
    margin-bottom: 1rem;
}

.card-body {
    max-width: 150px;

    text-align: left;
    color: #fff;

    h5 {
        font-weight: 600;
        margin-bottom: 1rem;
    }

}

@media screen and (max-width: 1080px) {

    .card {
        margin-left: 25px;
    }
}
</style>