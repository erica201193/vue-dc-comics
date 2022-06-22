<template>
    <footer>
        <div class="bg-blue">
            <div class="container">
                <div class="row text-light py-5">
                    <div class="col d-flex justify-content-center align-items-center" v-for="(link, i) in bannerLinks" :key="i">
                        <img :src="link.url" alt="">
                        <a href="link.href" class="text-light text-decoration-none ps-2">{{ link.name }}</a>
                    </div>
                </div>
            </div>
        </div>

        <div class="footer-bg-image">
            <div class="container">
                <div class="row text-light justify-content-between">
                    <div class="col-4 d-flex py-5">
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
                    <div class="col-6 p-0 logo-container">
                        <img src="/img/dc-logo-bg.png" alt="">
                    </div>
                    <!-- <div class="col-6 logo-container">
                        <img src="/img/dc-logo-bg.png" alt="">
                    </div> -->
                </div>
            </div>
        </div>

        
        <div class="bg-grey">
            <div class="container">
                <div class="row justify-content-between align-items-center py-1">
                    <div class="col-2">
                        <a href="#" class="text-uppercase fw-bold signup-btn">Sign-up now!</a>
                    </div>
                    <div class="col d-flex align-items-center justify-content-end">
                        <a href="#" class="text-uppercase fw-bold follow-btn ">Follow us</a>

                        <a class="p-1" v-for="link in socialLinks" :key="link.name">
                            <img :src="link.url" alt="">
                        </a>


                    </div>
                </div>
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
            ],
            socialLinks: [
                {
                    name: "Facebook",
                    href: "#",
                    url: "/img/footer-facebook.png" 
                },
                {
                    name: "Twitter",
                    href: "#",
                    url: "/img/footer-twitter.png" 
                },
                                {
                    name: "You Tube",
                    href: "#",
                    url: "/img/footer-youtube.png" 
                },
                {
                    name: "Pinterest",
                    href: "#",
                    url: "/img/footer-pinterest.png" 
                },
                {
                    name: "Periscope",
                    href: "#",
                    url: "/img/footer-periscope.png" 
                }
            ]

        }
    }
}
</script>

<style lang="scss" scoped>
.bg-blue {
    background-color: rgb(4, 130, 249);
    font-weight: bold;


    img {
        width: 40px;
    }
}

.bg-grey {
    background-color: #303030;
    color: white;
    padding: 20px;
}



.footer-bg-image {
    background-image: url("/public/img/footer-bg.jpg");
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;


    .row {
        font-size: 0.8rem;
        
        h5 {
            font-size: 1.2rem;
        }
    }


.logo-container {
    height: 363px;
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
    img{
        height: 155%;
        
    }
}
}
.signup-btn {
    text-decoration: none;
    font-size: 1.2rem;
    color: white;
    border: 2px solid rgb(4, 130, 249);
    padding: .6rem 1rem;

    &:hover {
        color: rgb(4, 130, 249);
    }
}

.follow-btn {
    text-decoration: none;
    font-size: 1.2rem;
    color: rgb(4, 130, 249);
    border: 2px solid transparent;
    padding: .6rem 1rem;
    margin-left: 0.5rem;

    &:hover {
        border: 2px solid white;
    }
}
</style>