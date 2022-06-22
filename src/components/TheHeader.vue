<template>
    <div>
        <div class="row py-4">
            <div class="col-1 g-0 d-flex">
                <img src="/img/dc-logo.png" alt="" class="logo">
            </div>

            <div class="col d-flex justify-content-end align-items-center">
                <ul class="nav h-100 ">
                    <li class="nav-item d-flex align-items-center" v-for="(link, i) in navLinks" :key="i">
                        <a class="nav-link my-nav-link text-center" aria-current="page" :href="link.href">
                        {{ link.name }}
                        <div class="select-underline"></div>
                        </a>
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
    color: #706f6f;
    font-weight: bold;

    &:hover {
        color: #0482F9;
        .select-underline {
            opacity: 100%;
        }
    }

    &:focus {
        color: #0482F9;
        .select-underline {
            opacity: 100%;
        }
    }
}
.select-underline {
    width: 40px;
    margin: auto;
    border: 2px solid #0482F9;
    transform: translate(0px, 40px);
    opacity: 0%;
}
</style>