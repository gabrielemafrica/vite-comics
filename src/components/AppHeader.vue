<script>
export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    text: "Characters",
                    url: "#",
                    current: false,
                },
                {
                    text: "Comics",
                    url: "#",
                    current: true,
                },
                {
                    text: "Movies",
                    url: "#",
                    current: false,
                },
                {
                    text: "Tv",
                    url: "#",
                    current: false,
                },
                {
                    text: "Games",
                    url: "#",
                    current: false,
                },
                {
                    text: "Collectibles",
                    url: "#",
                    current: false,
                },
                {
                    text: "Videos",
                    url: "#",
                    current: false,
                },
                {
                    text: "Fans",
                    url: "#",
                    current: false,
                },
                {
                    text: "News",
                    url: "#",
                    current: false,
                },
                {
                    text: "Shop",
                    url: "#",
                    current: false,
                },

            ]
        }
    }
}

</script>

<template>
    <header>
        <div class="container">

            <a href="/" class="brand">
                <img src="/dc-logo.png" alt="dc">
            </a>

            <nav>
                <ul>
                    <li v-for="link in links">
                        <a :href="link.url" :class="{ active: link.current }">{{ link.text }}</a>
                    </li>

                </ul>
            </nav>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

header {
    // text-align: center;
    height: 100px;

    .container {
        display: flex;
        align-items: center;
        justify-content: space-between;
        height: 100%;

        .brand {
            width: 80px;
            height: 100%;
            @include center();
            align-items: center;
        }

        nav {
            height: 100%;

            ul {

                list-style-type: none;
                margin: 0;
                @include center();
                height: 100%;

                li {
                    height: 100%;

                    a {
                        height: 100%;
                        text-transform: uppercase;
                        display: inline-block;
                        padding: 2rem 0;
                        margin: 0 1rem;
                        text-decoration: none;
                        font-weight: 600;
                        font-size: 12px;
                        transition: background 0.3s;

                        &.active,
                        &:hover {
                            // background-color: lighten($primary, 90%);
                            // background-color: $primary;
                            color: $primary;
                            border-bottom: 5px solid $primary;
                        }
                    }
                }
            }
        }
    }
}
</style>
