<script>
export default {
    name: "AppFooter",
    methods: {
        getImageURL: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    },
    data() {
        return {
            sectionsLinks: [
                {
                    title: "dc comics",
                    links: [
                        {
                            title: "Characters",
                            url: "#",
                            current: false,
                        },
                        {
                            title: "Comics",
                            url: "#",
                            current: false,
                        },
                        {
                            title: "Movies",
                            url: "#",
                            current: false,
                        },
                        {
                            title: "TV",
                            url: "#",
                            current: false,
                        },
                        {
                            title: "Games",
                            url: "#",
                            current: false,
                        },
                        {
                            title: "Videos",
                            url: "#",
                            current: false,
                        },
                        {
                            title: "News",
                            url: "#",
                            current: false,
                        },

                    ],
                },
                {
                    title: "dc",
                    links: [
                        {
                            title: "Terms Of Use",
                            url: "#",
                            current: false,
                        },
                        {
                            title: "Privacy policy (New)",
                            url: "#",
                            current: false,
                        },
                        {
                            title: "Ad Choices",
                            url: "#",
                            current: false,
                        },
                        {
                            title: "Advertising",
                            url: "#",
                            current: false,
                        },
                        {
                            title: "Jobs",
                            url: "#",
                            current: false,
                        },
                        {
                            title: "Subscriptions",
                            url: "#",
                            current: false,
                        },
                        {
                            title: "Talent Workshops",
                            url: "#",
                            current: false,
                        },
                        {
                            title: "CPSC Certificates",
                            url: "#",
                            current: false,
                        },
                        {
                            title: "Ratings",
                            url: "#",
                            current: false,
                        },
                        {
                            title: "Shop Help",
                            url: "#",
                            current: false,
                        },
                        {
                            title: "Contact US",
                            url: "#",
                            current: false,
                        },

                    ],
                },
                {
                    title: "Sites",
                    links: [
                        {
                            title: "DC",
                            url: "#",
                            current: false,
                        },
                        {
                            title: "MAD Magazine",
                            url: "#",
                            current: false,
                        },
                        {
                            title: "DC Kids",
                            url: "#",
                            current: false,
                        },
                        {
                            title: "DC Universe",
                            url: "#",
                            current: false,
                        },
                        {
                            title: "DC Power Visa",
                            url: "#",
                            current: false,
                        },
                    ],
                },
                {
                    title: "Shop",
                    links: [
                        {
                            title: "Shop DC",
                            url: "#",
                            current: false,
                        },
                        {
                            title: "Shop DC Collectibles",
                            url: "#",
                            current: false,
                        },
                    ],
                },


            ]
        }
    }
}

</script>

<template>
    <footer>
        <!-- footer topper -->
        <!-- footer centre -->
        <div class="f-centre">
            <div class="container">
                <div class="footer-links">
                    <div class="links-section" v-for="section in sectionsLinks">
                        <h4>{{ section.title }}</h4>
                        <nav>
                            <ul>
                                <li v-for="link in section.links">
                                    <a :href="link.url" :class="{ active: link.current }">
                                        {{ link.title }}
                                    </a>
                                </li>
                            </ul>
                        </nav>
                    </div>
                </div>
                <div class="footer-logo">
                    <img :src="getImageURL('../assets/images/dc-logo-bg.png')" />
                </div>
            </div>
        </div>

        <!-- footer bottom -->
        <div class="cols container">
            <a class="logo" href="/">
                <img src="/dc-logo.png" alt="dc">
            </a>

            <div class="footer-links">
                <h4>DC</h4>

                <nav>
                    <ul>
                        <li><a href="#">Link</a></li>
                        <li><a href="#">Link</a></li>
                        <li><a href="#">Link</a></li>
                        <li><a href="#">Link</a></li>
                        <li><a href="#">Link</a></li>
                    </ul>
                </nav>
            </div>
            <div class="footer-links">
                <h4>DC</h4>

                <nav>
                    <ul>
                        <li><a href="#">Link</a></li>
                        <li><a href="#">Link</a></li>
                        <li><a href="#">Link</a></li>
                        <li><a href="#">Link</a></li>
                        <li><a href="#">Link</a></li>
                    </ul>
                </nav>

            </div>
        </div>
        <img :src="getImageURL(`../assets/images/footer-bg.jpg`)" alt="dc">
    </footer>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

footer {

    color: white;


    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;

    }

    .f-centre {

        background-image: url(../assets/images/footer-bg.jpg);
        background-size: cover;

        .links-section {

            float: left;
            width: calc(100% / 3);

            h4 {
                text-transform: uppercase;
            }

            ul {
                list-style-type: none;
                margin: 0;
                padding: 0;

                li a {
                    color: white;
                    text-decoration: none;

                    &:hover {
                        color: $primary;
                    }
                }
            }
        }

        .footer-logo {


            img {
                object-fit: contain;
            }
        }
    }


    .cols {
        display: flex;
        margin-bottom: 3rem;

        .logo,
        .footer-links {
            flex-basis: calc(100% / 3);
            padding: 0 1rem;
        }

        h4 {
            text-transform: uppercase;
            font-size: 1.25rem;
            font-weight: 600;
            margin-bottom: 1rem;
        }

        ul {
            list-style: none;

            li a {


                display: inline-block;
                margin-bottom: 0.25rem;
                text-decoration: none;
                font-size: 0.875em;

                &:hover {
                    color: $primary;
                }
            }
        }
    }
}
</style>
