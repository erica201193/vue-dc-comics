<template>
    <div class="product-card">
        <div class="py-2 image-container">
            <img :src="imgUrl" :alt="`Immagine di ${cardTitle}`">
            <div class="card-price">{{ cardPrice }}</div>      
        </div>
        <div class="pt-3 text-uppercase">{{ cardTitle }}</div>
        <div class="card-type text-capitalize">{{ cardType }}</div>

    </div>
</template>

<script>
export default{
props: {
    cardTitle: String,
    imgUrl: String,
    cardPrice: String,
    cardType: String,
}
}
</script>

<style lang="scss" scoped>
.product-card {
    color: white;

    & img {
        width: 100%;
        aspect-ratio: 1/1;
        object-fit: cover;
        object-position: top;
    }
    & .card-type {
        color: #0482f9;
    }

    & .image-container {
        position: relative;
        & .card-price {
            color: black;
            background-color: #F7CA00;
            text-align: end;
            border-radius: 5px;
            display: inline-block;
            padding: 0.2rem 0.8rem;
            margin-top: 1rem;
            position: absolute;
            bottom:0px;
            right: 0;
        }
    }
}
</style>

