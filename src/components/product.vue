<template>
    <div>
        <h1>
            <font-awesome-icon icon="hammer"/>
            Product
        </h1>
        <div class="container">
            <div class="item">
                <div class="card">
                    <img class="card-img" src="../assets/note.jpg">
                    <div class="card-content">
                        <h1 class="card-title">What did I do.</h1>
                        <p class="card-text">
                            過去にやってきたことはこちらにまとめてあります。<br>
                        </p>
                    </div>
                    <div class="card-link">
                        <a href="https://www.wantedly.com/id/mitsui321">
                            <button class="button-blue">Wantedly</button>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "product",
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
.card {
    width: 350px;
    background: #fff;
    border-radius: 5px;
    box-shadow: 0 2px 5px #ccc;
}
.card-img {
    border-radius: 5px 5px 0 0;
    max-width: 100%;
    height: auto;
}
.card-content {
    padding: 20px;
}
.card-title {
    font-size: 20px;
    margin-bottom: 20px;
    text-align: center;
    color: #333;
}
.card-text {
    color: #777;
    font-size: 14px;
    line-height: 1.5;
}
.card-link {
    text-align: center;
    border-top: 1px solid #eee;
    padding: 20px;
}
.card-link a {
    text-decoration: none;
    color: #0bd;
    margin: 0 10px;
}
.card-link a:hover {
    color: #0090aa;
}

.button-blue {
    color: white;
    padding: 7px 30px;
    border: none;
    border-radius: 4px;
    background-color: gray;
    outline: none;
}

</style>
