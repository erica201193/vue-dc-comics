<template>
    <div>
        <div class="container">
            <div class="row">
                <div class="col-4">
                    <img src="/img/dc-logo.png" alt="">
                </div>

                <div class="col-8">
                    <ul class="nav">
                        <li class="nav-item" v-for="(link, i) in navLinks" :key="i">
                            <a class="nav-link active" aria-current="page" :href="link.href">{{ link.name }}</a>
                        </li>
                    </ul>
                </div>
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

<style>
</style>