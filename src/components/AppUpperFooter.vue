<script>
export default {
    name: "AppUpperFooter",
    data() {
        return {
            sections: [
                {
                    title: "Digital Comics",
                    src: "src/assets/images/buy-comics-digital-comics.png",
                    link: "#",
                    current: false,
                },
                {
                    title: "Dc Merchandise",
                    src: "src/assets/images/buy-comics-merchandise.png",
                    link: "#",
                    current: false,
                },
                {
                    title: "Subscription",
                    src: "src/assets/images/buy-comics-subscriptions.png",
                    link: "#",
                    current: false,
                },
                {
                    title: "Comic Shop Locator",
                    src: "src/assets/images/buy-comics-shop-locator.png",
                    link: "#",
                    current: false,
                },
                {
                    title: "Dc Power Visa",
                    src: "src/assets/images/buy-dc-power-visa.svg",
                    link: "#",
                    current: false,
                },
            ]

        }
    }
}

</script>

<template>
    <div class="upper-footer">
        <div class="container">
            <ul>
                <li v-for="(section, index) in sections" :key="index">
                    <a class="container-section">
                        <div>
                            <img :src="section.src" :alt="section.title">
                        </div>
                        <span class="container-section-title">{{ section.title }}</span>
                    </a>
                </li>
            </ul>

        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

.upper-footer {
    background-color: $primary;
    padding: 50px;

    .container {

        ul {
            display: flex;
            justify-content: space-around;
            align-items: center;
            list-style-type: none;
            margin: 0;
            padding: 0;

            li {


                a {
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    gap: 10px;
                    color: white;
                    text-transform: uppercase;
                    font-size: small;
                    cursor: pointer;

                    div {
                        width: 50px;
                        height: 50px;


                        img {
                            height: 100%;
                            width: 100%;
                            object-fit: contain;
                            object-position: center;

                        }
                    }

                    &:hover {
                        filter: opacity(50%);
                    }
                }
            }
        }
    }
}
</style>
