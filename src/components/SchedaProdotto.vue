<script>
export default {
    name: "SchedaProdotto",
    props: {
        details: Object,
        linkImg: String,
        nameImg: String
    }
}

</script>

<template>
    <div class="scheda">
        <div class="foto-scheda">
            <img :src="linkImg" :alt="nameImg">
        </div>
        <h4>{{ nameImg }}</h4>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.scheda {
    color: white;
    width: calc(100% / 6);
    padding: 10px;
    cursor: pointer;
    text-align: left;

    &:hover {
        filter: brightness(150%);
        color: $primary;
        outline: auto;
    }

    .foto-scheda {
        height: 180px;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: top;

        }
    }

    h4 {
        font-size: 12px;
        font-weight: normal;
        margin: 10px 0 20px 0;
        text-transform: uppercase;
    }
}
</style>
