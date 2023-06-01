<script>
import AppBottomFooter from './AppBottomFooter.vue'
import AppUpperFooter from './AppUpperFooter.vue'

export default {
    name: "AppFooter",
    methods: {
        getImageURL: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    },
    components: {
        AppBottomFooter,
        AppUpperFooter
    },
    data() {
        return {
            sectionsLinks: [
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
        <!-- footer upper -->
        <AppUpperFooter />
        <!-- footer centre -->
        <div class="f-centre">
            <div class="container">
                <div class="footer-links">
                    <div class="links-section" v-for="(section, index) in sectionsLinks" :key="index">
                        <h4>{{ section.title }}</h4>
                        <nav>
                            <ul>
                                <li v-for="(link, index) in section.links" :key="index">
                                    <a :href="link.url" :class="{ active: link.current }">
                                        {{ link.title }}
                                    </a>
                                </li>
                            </ul>
                        </nav>
                    </div>
                </div>
            </div>
        </div>

        <!-- footer bottom -->
        <AppBottomFooter />
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

        background-image: url(../assets/images/dc-logo-bg.png), url(../assets/images/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: 25%, cover;
        background-position-x: 80%, 0;
        background-position-y: center, 0;
        padding: 40px 0;


        .links-section {

            float: right;
            width: calc(100% / 3);

            h4 {
                text-transform: uppercase;
                margin-bottom: 10px;
            }

            ul {
                list-style-type: none;
                margin: 0;
                padding: 0;
                margin-bottom: 10px;



                li a {
                    color: white;
                    text-decoration: none;
                    font-size: 12px;
                    font-weight: lighter;


                    &:hover {
                        color: $primary;
                    }
                }
            }
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
</style>
