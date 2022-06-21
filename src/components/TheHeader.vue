<template>
    <div>
        <div class="row py-3">
            <div class="col-1 g-0 d-flex">
                <img src="/img/dc-logo.png" alt="" class="logo">
            </div>

            <div class="col d-flex justify-content-end align-items-center">
                <ul class="nav">
                    <li class="nav-item" v-for="(link, i) in navLinks" :key="i">
                        <a class="nav-link my-nav-link" aria-current="page" :href="link.href">{{ link.name }}</a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>


<script>
export default {
    name: "TheHeader",
    data() {
        return {
            navLinks: [
                {
                    name: "CHARACTERS",
                    href: "#"
                },
                {
                    name: "COMICS",
                    href: "#"
                },
                {
                    name: "MOVIES",
                    href: "#"
                },
                {
                    name: "TV",
                    href: "#"
                },
                {
                    name: "GAMES",
                    href: "#"
                },
                {
                    name: "COLLECTIBLES",
                    href: "#"
                },
                {
                    name: "VIDEOS",
                    href: "#"
                },
                {
                    name: "FANS",
                    href: "#"
                },
                {
                    name: "NEWS",
                    href: "#"
                },
                {
                    name: "SHOP",
                    href: "#"
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.logo {
    width: 60px;

}
.my-nav-link {
    font-size: 0.8rem;

    &:hover {
        border-bottom: 5px solid blue;
    }
}
</style>