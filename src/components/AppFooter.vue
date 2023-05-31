<script>
export default {
    name: "AppFooter",
    methods: {
        getImageURL: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
}

</script>

<template>
    <footer>
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
    padding-top: 3rem;

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
