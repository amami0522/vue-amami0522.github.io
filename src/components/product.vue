<template>
    <div>
        <h1>
            <font-awesome-icon icon="hammer"/>
            Product
        </h1>
        <div class="container">
<!--            <div class="item">-->
<!--                <div class="card">-->
<!--                    <img class="card-img" src="../assets/note.jpg">-->
<!--                    <div class="card-content">-->
<!--                        <h1 class="card-title">What did I do.</h1>-->
<!--                        <p class="card-text">-->
<!--                            過去にやってきたことはこちらにまとめてあります。<br>-->
<!--                        </p>-->
<!--                    </div>-->
<!--&lt;!&ndash;                    <div class="card-link">&ndash;&gt;-->
<!--&lt;!&ndash;                        <a href="https://www.wantedly.com/id/mitsui321">&ndash;&gt;-->
<!--&lt;!&ndash;                            <button class="button-blue">Wantedly</button>&ndash;&gt;-->
<!--&lt;!&ndash;                        </a>&ndash;&gt;-->
<!--&lt;!&ndash;                    </div>&ndash;&gt;-->
<!--                </div>-->
<!--            </div>-->
            <div class="item">
                <div class="card">
                    <img class="card-img" src="../assets/news.png">
                    <div class="card-content">
                        <h1 class="card-title">News Gacha Simulator</h1>
                    </div>
                </div>
            </div>
            <div class="item">
                <div class="card">
                    <img class="card-img" src="../assets/koyofes.jpg">
                    <div class="card-content">
                        <h1 class="card-title">足で音を鳴らすキーボード</h1>
                    </div>
                </div>
            </div>
            <div class="item">
                <div class="card">
                    <img class="card-img" src="../assets/maze.png">
                    <div class="card-content">
                        <h1 class="card-title">迷路生成 最短経路探索</h1>
                    </div>
                </div>
            </div>
            <div class="item">
                <div class="card">
                    <img class="card-img" src="../assets/chat.png">
                    <div class="card-content">
                        <h1 class="card-title">GET</h1>
                    </div>
                </div>
            </div>
            <div class="item">
                <div class="card">
                    <img class="card-img" src="../assets/competitive.jpg">
                    <div class="card-content">
                        <h1 class="card-title">競技プログラミングコンテスト<br>への参加</h1>
                        <button class="button-blue" @click="openModal5()">詳しく見る</button>
                    </div>
                </div>
            </div>
        </div>
        <div class="modal-overlay" v-if="isShown5">
            <div class="modal-window">
                <div class="modal-content">
                    <h2>競技プログラミングコンテストへの参加</h2>
                    <p class="modal-text">
                        趣味で競技プログラミングをやっています。<br>
                        普段はAtCoderを中心に活動していて、その他コンテストにも参加させていただいています。<br>
                        使用言語は主にC++とPythonです。<br>
                        参加コンテストについては以下の通りになっています。<br>
                    </p>
                    <div class="contests">
                        <p class="contest-name">情報オリンピック2017, 2018</p>
                        <p class="contest-name">パソコン甲子園2018, 2019</p>
                        <p class="contest-name">全国高専プロコン大30回都城大会 競技部門</p>
                        <p class="contest-name">PG BATTLE 2019, 2020</p>
                        <p class="contest-name"> Google Code Jam 2020, 2021 Round1</p>
                        <p class="contest-name">ICPC 2020 Asia Yokohama Regional qualifying round</p>
                    </div>
                    <button class="button-blue" @click="closeModal5()">閉じる</button>
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
            isShown1: false,
            isShown2: false,
            isShown3: false,
            isShown4: false,
            isShown5: false
        }
    },
    methods: {
        openModal1() { this.isShown1 = true; },
        openModal2() { this.isShown2 = true; },
        openModal3() { this.isShown3 = true; },
        openModal4() { this.isShown4 = true; },
        openModal5() { this.isShown5 = true; },
        closeModal1() { this.isShown1 = false; },
        closeModal2() { this.isShown2 = false; },
        closeModal3() { this.isShown3 = false; },
        closeModal4() { this.isShown4 = false; },
        closeModal5() { this.isShown5 = false; }
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
    width: 300px;
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
.modal-overlay {
    display: flex;
    align-items: center;
    justify-content: center;
    position: fixed;
    z-index: 30;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
}
.modal-window {
    background: #fff;
    border-radius: 4px;
    overflow: hidden;
    max-width: 90%;
    max-height: 70%;
    overflow-y: auto;
}
.modal-content {
    padding: 10px 20px;
}
.modal-text {
    color: gray;
    text-align: center;
    line-height: 30px;
}
.contests {
    margin: 40px;
}
.contest-name {
    color: gray;
}
</style>
