<template>
    <div class="product-card">
        <img :src="imgUrl" :alt="`Immagine di ${cardTitle}`">
        <div class="py-3">{{ cardTitle }}</div>

    </div>
</template>

<script>
export default{
props: {
    cardTitle: String,
    imgUrl: String
}
}
</script>

<style lang="scss" scoped>
.product-card {
    color: white;
    text-transform: uppercase;
    & img {
        width: 100%;
        aspect-ratio: 1/1;
        object-fit: cover;
        object-position: top;
    }
}
</style>

