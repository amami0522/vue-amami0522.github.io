<template>
    <div>
        <header class="cover">
            <h1>Amami's portfolio</h1>
        </header>
    </div>
</template>

<script>
export default {
    name: "titleBackground",
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

header {
    position: relative;
    height: 30vh;
    background: url("../assets/header.jpg") center / cover;
}

header h1 {
    position: absolute;
    z-index: 1;
    top: 50%;
    width: 100%;
    margin: 0;
    padding: 0;
    font-size: 4rem;
    color: #fff;
}

.cover::after {
    content: "";
    display: block;
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background: rgba(0,0,0,.3) radial-gradient(rgba(0,0,0,.3) 25%, transparent 0) center / 5px 5px;
}

@media all and (max-width: 480px) {
    header h1 {
        font-size: 2rem;
    }
}

.name {
    margin: 50px auto;
}

</style>
