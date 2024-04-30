<script>
export default {
    data() {
        return {
            title: "Banner title",
            image: "rende.jpg"
        };
    },
    methods: {
        getImagePath(imageName) {
            return new URL(`../assets/img/${imageName}`, import.meta.url).href;
        },
    },
};
</script>

<template>
    <div class="banner">
        <h2>{{ title }}</h2>
        <img :src="getImagePath(image)" alt="">
    </div>
</template>

<style>
img {
    max-width: 100%;
}

.banner {
    position: relative;
}
</style>