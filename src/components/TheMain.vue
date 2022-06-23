<template>
    <div class="products-container">

        <div class="jumbo-bg-image">
            <img src="/img/jumbotron.jpg" alt="" v-if="currentIndex === null ">
        </div>
        <div class="row row-cols-1 pt-3 selected-product" v-if="currentIndex !== null">
            <div class="col text-light text-center fw-bold text-uppercase fs-2 p-4 " >{{products[currentIndex].series }}</div>
            <img :src="products[currentIndex].thumb" alt="" class="col g-0">
            <div class="col text-light text-center text-uppercase fs-4 p-4">{{ products[currentIndex].price }}</div>
        </div>

        <div class="container">
            <div class="main-series-title">
                <h5 class="text-uppercase" >Current series</h5>
            </div>
            <div class="row row-cols-6">
                <div class="col pt-2 pb-4" v-for="(product,i) in products" :key="product.series" @click="slider(i)">
                    <ProductCard :card-title="product.series"
                    :imgUrl="product.thumb" :card-type="product.type" :card-price="product.price"></ProductCard>
                </div>
            </div>
        </div>
        
    </div>
</template>

<script>
import ProductCard from './ProductCard.vue';
export default {
    components: { ProductCard },
    data() {
        return {
            products: [
                {
                thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                price: "$19.99",
                series: "Action Comics",
                type: "comic book",
                },
                {
                thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                price: "$3.99",
                series: "American Vampire 1976",
                type: "comic book",
                },
                {
                thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                price: "$16.99",
                series: "Aquaman",
                type: "graphic novel",
                },
                {
                thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                price: "$2.99",
                series: "Batgirl",
                type: "comic book",
                },
                {
                thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                price: "$3.99",
                series: "Batman",
                type: "comic book",
                },
                {
                thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                price: "$2.99",
                series: "Batman Beyond",
                type: "comic book",
                },
                {
                thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                price: "$3.99",
                series: "Batman/Superman",
                type: "comic book",
                },
                {
                thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                price: "$4.99",
                series: "Batman/Superman Annual",
                type: "comic book",
                },
                {
                thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                price: "$5.99",
                series: "Batman: The Joker War Zone",
                type: "comic book",
                },
                {
                thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                price: "$6.99",
                series: "Batman: Three Jokers",
                type: "comic book",
                },
                {
                thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                price: "$4.99",
                series: "Batman: White Knight Presents: Harley Quinn",
                type: "comic book",
                },
                {
                thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                price: "$16.99",
                series: "Catwoman",
                type: "graphic novel",
                },
            ],
            currentIndex: null,
        };
    },

    methods: {
        slider(index) {
            this.currentIndex = index;

            console.log(`sei all'indice numero ${this.currentIndex} `)
        }
    }
};
</script>

<style lang="scss" scoped>

.jumbo-bg-image {
    & img {
        width: 100%;
        height: 400px;
        object-fit: none;
        object-position: top;
    }
}

.selected-product {
    justify-content: center;
    align-items: center;
    & img {
        width: 20%;
        height: 400px;
        object-position: center;
        box-shadow: 0px 1rem 3rem rgba($color: #ffff, $alpha: 0.175)
    }
}
.main-series-title {
    & h5 {
        font-size: 2rem;
        color: white;
        font-weight: bold;
        padding: 0.6rem 2rem;
        background-color: #0482f9;
        display: inline-block;
        position: relative;
        bottom: 30px;
        box-shadow: .5rem .5rem 1rem rgba(#0482f9, .3);
    }
}
</style>
