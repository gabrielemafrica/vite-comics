<script>
export default {
    name: "AppBottomFooter",
    data() {
        return {
            ikons: [
                {
                    title: "Facebook",
                    src: "src/assets/images/footer-facebook.png",
                    link: "#",
                    current: false,
                },
                {
                    title: "Twitter",
                    src: "src/assets/images/footer-twitter.png",
                    link: "#",
                    current: false,
                },
                {
                    title: "Youtube",
                    src: "src/assets/images/footer-youtube.png",
                    link: "#",
                    current: false,
                },
                {
                    title: "Pinterest",
                    src: "src/assets/images/footer-pinterest.png",
                    link: "#",
                    current: false,
                },
                {
                    title: "Periscope",
                    src: "src/assets/images/footer-periscope.png",
                    link: "#",
                    current: false,
                },
            ]

        }
    }
}

</script>

<template>
    <div class="bottom-footer">
        <div class="container">
            <button>SIGN-UP NOW!</button>
            <div class="follow">
                <h4>FOLLOW US</h4>
                <ul>
                    <li v-for="(ikon, index) in ikons" :key="index">
                        <a class="container-social">
                            <!-- <img src="../assets/images/footer-periscope.png"> -->
                            <img :src="ikon.src" :alt="ikon.title">
                        </a>
                    </li>
                </ul>

            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

.bottom-footer {
    background-color: rgb(48, 48, 48);
    padding: 30px 0;

    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;

        button {
            border-radius: 0;
            background-color: transparent;
            color: white;
            font-size: 16px;
            font-weight: bold;
            padding: 10px 20px;
            border: 2px solid $primary;
            cursor: pointer;
            text-transform: uppercase;
            transition: background 0.3s;

            &:hover {
                background-color: $primary;
            }
        }

        .follow {
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 20px;


            h4 {
                color: $primary;
            }

            ul {
                display: flex;
                justify-content: space-between;
                align-items: center;
                gap: 20px;
                list-style-type: none;
                margin: 0;
                padding: 0;

                li a {
                    cursor: pointer;

                    &:hover img {
                        filter: brightness(100);
                    }
                }
            }
        }
    }
}
</style>
