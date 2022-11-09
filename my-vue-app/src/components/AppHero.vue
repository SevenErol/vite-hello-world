<script>

export default {
    data() {
        return {
            imageName: "one piece jumbotron.webp"
        }
    },

    methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
};

</script>

<template>
    <div class="container">
        <img class="jumbo" :src="getImagePath(`../assets/${imageName}`)" alt="">
    </div>
</template>

<style scoped>
.container {
    width: 60%;
    margin: auto;
}

.jumbo {
    max-width: 100%;
}
</style>