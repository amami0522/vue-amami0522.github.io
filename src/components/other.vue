<template>
    <div>
        <h1>
            <font-awesome-icon icon="address-book"/>
            Others
        </h1>
        <div class="container">
            <div class="item">
                <a href="https://twitter.com/amimami_0522" target="_blank">
                    <img src="../assets/Twitter_Social_Icon_Circle_Color.png">
                </a>
            </div>
            <div class="item">
                <a href="https://github.com/amami0522?tab=overview" target="_blank">
                    <img src="../assets/GitHub-Mark-120px-plus.png">
                </a>
            </div>
            <div class="item">
                <a href="https://www.facebook.com/profile.php?id=100022663904491" target="_blank">
                    <img src="../assets/f_logo_RGB-Hex-Blue_512.png">
                </a>
            </div>
            <div class="item">
                <a href="https://t.co/YTEcOfIvt1" target="_blank">
                    <img src="../assets/hatenablog-logo.png">
                </a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "other",
    components: {
    },
    data: function() {
        return {
        }
    },
    methods: {
    },
}
</script>

<style scoped>

.container {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    margin: 50px auto;
    max-width: 750px;
}

.item {
    margin: 30px;
}

img {
    width: 75px;
}

</style>
