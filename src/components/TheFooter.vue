<template>
    <footer>
        <div class="bg-blue">
            <div class="container">
                <div class="row text-light">
                    <div class="col" v-for="(link, i) in bannerLinks" :key="i">
                        <div>
                            <img :src="link.url" alt="" width="40">
                            <a href="link.href" class="text-light">{{ link.name }}</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="footer-bg-image">
            <div class="container position-relative">
                <div class="row text-light py-5">
                    <div class="col-4 d-flex">
                        <div class="col">
                        <h5 class="text-uppercase fw-bold">Dc comics</h5>
                        <ul class="list-unstyled">
                            <li v-for="link in comicsLinks" :key="link"> {{link}}</li>
                        </ul>

                        <h5 class="text-uppercase fw-bold">Shop</h5>
                        <ul class="list-unstyled">
                            <li v-for="link in shopLinks" :key="link"> {{link}}</li>
                        </ul>
                    </div>
                    <div class="col">
                        <h5 class="text-uppercase fw-bold">Dc</h5>
                        <ul class="list-unstyled">
                            <li v-for="link in dcLinks" :key="link"> {{link}}</li>
                        </ul>
                    </div>
                    <div class="col">
                        <h5 class="text-uppercase fw-bold">Sites</h5>
                        <ul class="list-unstyled">
                            <li v-for="link in sitesLinks" :key="link"> {{link}}</li>
                        </ul>
                    </div>
                    </div>
                </div>
                <div class="logo-container">
                    <img src="/img/dc-logo-bg.png" alt="" class="position-absolute footer-logo">
                </div>
            </div>
        </div>

        <div class="row">
            <div class="col">signup</div>
            <div class="col"></div>
        </div>
    </footer>
</template>


<script>
export default {
    name: "TheFooter",
    data() {
        return {
            bannerLinks: [
                {
                    name: "DIGITAL COMICS",
                    href: "#",
                    url: "/img/buy-comics-digital-comics.png" 
                },
                {
                    name: "DC MERCHANDISE",
                    href: "#",
                    url: "/img/buy-comics-merchandise.png" 
                },
                                {
                    name: "SUBSCRIPTION",
                    href: "#",
                    url: "/img/buy-comics-subscriptions.png" 
                },
                {
                    name: "COMIC SHOP LOCATOR",
                    href: "#",
                    url: "/img/buy-comics-shop-locator.png" 
                },
                {
                    name: "DC POWER VISA",
                    href: "#",
                    url: "/img/buy-dc-power-visa.svg" 
                }
            ],
            comicsLinks: [
                "Characters",
                "Comics",
                "Movies",
                "TV",
                "Games",
                "Videos",
                "News",
            ],
            shopLinks: [
                "Shop DC",
                "Shop C Collectibles",
            ],
            dcLinks: [
                "Terms Of Use",
                "Privacy policy (New)",
                "Ad Choices",
                "Advertising",
                "Jobs",
                "Subscriptions",
                "Talent Workshops",
                "CPSC Certificates",
                "Ratings",
                "Shop Help",
                "Contact Us",
            ],
            sitesLinks: [
                "DC",
                "MAD Magazine",
                "DC Kids",
                "DC Universe",
                "DC Power Visa",
            ]

        }
    }
}
</script>

<style lang="scss" scoped>
.bg-blue {
    background-color: rgb(4, 130, 249);
}

.footer-bg-image {
    background-image: url("/public/img/footer-bg.jpg");
    background-position: center;
    background-size: contain;

    .row {
        font-size: 0.8rem;
        
        h5 {
            font-size: 1rem;
        }
    }
.footer-logo {
    width: 530px;
    position: absolute;
    top: -90px;
    right:0;
    overflow: hidden;



}
}
</style>