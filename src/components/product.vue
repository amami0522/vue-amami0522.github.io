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
                        <button class="button-blue" @click="openModal1()">詳しく見る</button>
                    </div>
                </div>
            </div>
            <div class="item">
                <div class="card">
                    <img class="card-img" src="../assets/koyofes.jpg">
                    <div class="card-content">
                        <h1 class="card-title">足で音を鳴らすキーボード</h1>
                        <button class="button-blue" @click="openModal2()">詳しく見る</button>
                    </div>
                </div>
            </div>
            <div class="item">
                <div class="card">
                    <img class="card-img" src="../assets/maze.png">
                    <div class="card-content">
                        <h1 class="card-title">迷路生成 最短経路探索</h1>
                        <button class="button-blue" @click="openModal3()">詳しく見る</button>
                    </div>
                </div>
            </div>
            <div class="item">
                <div class="card">
                    <img class="card-img" src="../assets/chat.png">
                    <div class="card-content">
                        <h1 class="card-title">GET</h1>
                        <button class="button-blue" @click="openModal4()">詳しく見る</button>
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
        <div class="modal-overlay" v-if="isShown1">
            <div class="modal-window">
                <div class="modal-content">
                    <h2>News Gacha Simulator</h2>
                    <p><img src="../assets/news1.png" class="modal-image"></p>
                    <p class="modal-text">
                        インターンシップの事前課題としてJavascriptの勉強を兼ねて作成しました。<br>
                        NewsAPIを利用して、ボタンを押したら最新のニュースを取得して、その中からランダムで10個表示しておすすめします。<br>
                        ニュースを読んで情報を収集したい気持ちはあったが、数が多く少しめんどくさくなってしまったことがこれを作ったきっかけです。<br>
                        Javascriptを用いた初めての開発で、非同期処理に悩まされましたがいい勉強のきっかけになりました。
                    </p>
                    <button class="button-blue" @click="closeModal1()">閉じる</button>
                </div>
            </div>
        </div>
        <div class="modal-overlay" v-if="isShown2">
            <div class="modal-window">
                <div class="modal-content">
                        <h2>足で音を鳴らすキーボード</h2>
                    <p><img src="../assets/koyofes.jpg" class="modal-image"></p>
                    <p class="modal-text">
                        文化祭の展示としてチームで作成しました。<br>
                        近年の情勢を鑑みて、人と人とが直接接触しないようにしながらも来場者に楽しんでもらえるようにしたいと、この作品を作りました。<br>
                        足で地面に設置してあるセンサー付きアクリル板を踏むことで、流れているBGMに合わせた音楽が鳴るようになっています。<br>
                        キーボードとありますが、1つの音を1つのアクリル板に割り当ててしまうと、すべての音を来場者が演奏しなければならなくなり、音楽を作るのが難しいといった点や、センサー付きアクリル板の制作コストといった点を考慮して音楽自体を鳴らすという構造になっています。<br>
                        私はPythonのWebSocketという技術を用いて、踏まれたことをセンサーが感知した情報をサーバ用のPCに送信する通信部分を担当しました。<br>
                        クライアント側のマシンとして手軽に用意できたRaspberry pi を使用したため、環境の違いや、Pythonのバージョンの違いに苦労したりしましたが、調べながらも最終的には動く形まで持っていくことが出来ました。<br>
                        大人数での開発となりましたが開発メンバーの中心として、チーム開発のいい経験になりました。
                    </p>
                    <button class="button-blue" @click="closeModal2()">閉じる</button>
                </div>
            </div>
        </div>
        <div class="modal-overlay" v-if="isShown3">
            <div class="modal-window">
                <div class="modal-content">
                    <h2>迷路生成 最短経路探索</h2>
                    <p><img src="../assets/maze1.png" class="modal-image"></p>
                    <p class="modal-text">
                        Javascriptでフロントエンドの勉強と、今まで競技プログラミングで得た経験が生かせないかと思い作成しました。<br>
                        フォームで指定したサイズの壁伸ばし法という迷路生成アルゴリズムを用いて迷路を自動で生成し、そこから幅優先探索というアルゴリズムを用いて最短経路を探す過程をJavascriptによってアニメーションのように可視化するといったものです。
                    </p>
                    <button class="button-blue" @click="closeModal3()">閉じる</button>
                </div>
            </div>
        </div>
        <div class="modal-overlay" v-if="isShown4">
            <div class="modal-window">
                <div class="modal-content">
                    <h2>GET</h2>
                    <p><img src="../assets/get1.png" class="modal-image"></p>
                    <p><img src="../assets/get2.png" class="modal-image"></p>
                    <p><img src="../assets/get3.png" class="modal-image"></p>
                    <p class="modal-text">
                        2020年に参加した株式会社jig.jpの夏季インターンシップにて作成しました。<br>
                        チームで「おうち時間」の課題を解決することを目的としたハッカソン形式でアジャイル開発を行いました。<br>
                        私たちのチームで話し合ったところ、同じ学年である大学1年生はほとんど学校に行けていないといったことが話題に上がりました。<br>
                        そのため、入学したばかりでオンライン授業になってしまい、時間はあるが交流が出来ていない大学1年生を主なターゲットとしたチャットアプリケーションを作成しました。<br>
                        概要としては、簡単な二択の質問を利用者に投げかけ、似たような興味を持った人たちを同じ話題の提供されたルームに集めて、トークしてもらうといったものです。<br>
                        自分はバックエンドの勉強としてJavascriptとDeno（javascript実行環境）を用いてサーバーサイドの開発を行いました。<br>
                        学生をターゲットとして作成を行ったので、スマートフォンへの対応を行ったのですが、iPhoneでの動作がうまくいかなかったりなどつまずいた点もありましたが、なんとか動く形に持っていくことが出来て良かったです。<br>
                        初めてアジャイル開発というものを経験して、動作させることを意識したために実装しきれなかったなど、まだ拙い部分も多かったですが、チーム開発のいい経験になりました。
                    </p>
                    <button class="button-blue" @click="closeModal4()">閉じる</button>
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
    max-height: 85%;
    overflow-y: auto;
}
.modal-content {
    padding: 10px 20px;
}
.modal-text {
    color: gray;
    /*text-align: center;*/
    text-align: left;
    line-height: 30px;
}
.modal-image {
    width: 100%;
    max-width: 600px;
}
.contests {
    margin: 40px;
}
.contest-name {
    color: gray;
}
</style>
