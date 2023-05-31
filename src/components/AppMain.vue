<script>
export default {
    name: "AppMain",
}

</script>

<template>
    <main>
        <div class="container">
            <h2>
                Content goes here
            </h2>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

main {
    background-color: black;
    padding: 50px 0;

    .container {
        display: flex;
        align-items: center;
        justify-content: space-between;

        h2 {
            color: white;
        }
    }
}
</style>
