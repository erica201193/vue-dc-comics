<template>
    <footer>
        <div class="row bg-primary text-light">
            <div class="col" v-for="(link, i) in bannerLinks" :key="i">
                <div>
                    <img :src="link.url" alt="" width="40">
                    <a href="link.href" class="text-light">{{ link.name }}</a>
                </div>
            </div>
        </div>
        <div class="row">
            <div class="col">
                <h5 class="text-uppercase">Dc comics</h5>
                <ul class="list-unstyled">
                    <li v-for="link in comicsLinks" :key="link"> {{link}}</li>
                </ul>

                <h5 class="text-uppercase">Shop</h5>
                <ul class="list-unstyled">
                    <li v-for="link in shopLinks" :key="link"> {{link}}</li>
                </ul>
            </div>
            <div class="col">
                <h5 class="text-uppercase">Dc</h5>
                <ul class="list-unstyled">
                    <li v-for="link in dcLinks" :key="link"> {{link}}</li>
                </ul>
            </div>
            <div class="col">
                <h5 class="text-uppercase">Sites</h5>
                <ul class="list-unstyled">
                    <li v-for="link in sitesLinks" :key="link"> {{link}}</li>
                </ul>
            </div>
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

<style>

</style>