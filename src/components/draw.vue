<template>
    <div>
        <h1>
            <font-awesome-icon icon="laptop-code"/>
            Competitive Programming
        </h1>
        <div class="graphArea">
            <lineChart :chart-data="datacollection" :option="options"/>
        </div>
        <h2>Other competition</h2>
        <div class="others">
            <div class="container">
                <div class="item">
                    <div class="card">
                        <img class="card-img" src="../assets/codeforces.jpg">
                        <div class="card-content">
                            <h1 class="card-title">Codeforces</h1>
                        </div>
                        <div class="card-link">
                            <a href="http://codeforces.com/profile/amami0522">
                                <button class="button-blue">Profile</button>
                            </a>
                        </div>
                    </div>
                </div>
                <div class="item">
                    <div class="card">
                        <img class="card-img" src="../assets/topcoder.jpg">
                        <div class="card-content">
                            <h1 class="card-title">Topcoder SRM</h1>
                        </div>
                        <div class="card-link">
                            <a href="https://www.topcoder.com/members/amami0522">
                                <button class="button-blue">Profile</button>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import lineChart from "@/components/lineChart";

export default {
    name: "draw",
    components: {
        lineChart
    },
    data: function() {
        return {
            datacollection: null,
            options: null,
        }
    },
    mounted() {
        this.fillData();
    },
    methods: {
        // 取得したAtCoderのレートをlineChart.jsに送るようにデータを編集
        fillData: function() {
            fetch("https://enigmatic-crag-08653.herokuapp.com/api/result")
            .then(res => {
                return res.json();
            })
            .then(json => {
                let year = "0";
                let graphLabels = [];  // グラフに表示されるラベル
                let graphRating = [];  // グラフに描画するレートのデータ
                for(let i = 0; i < json.length; i++) {
                    if(json[i]['IsRated']) {
                        // コンテスト終了の年を取得
                        const nowYear = json[i]['EndTime'].substr(0, 4);

                        // 年が更新されたらラベルに表示
                        if(nowYear !== year) { year = nowYear; graphLabels.push(year); }
                        else { graphLabels.push(""); }

                        // グラフの色を設定
                        graphRating.push(json[i]['NewRating']);
                    }
                }

                // グラフのオプションの設定
                this.options = {
                    responsive: true,
                    maintainAspectRatio: false,
                };
                // グラフのデータの設定
                this.datacollection = {
                    labels: graphLabels,
                    datasets: [
                        {
                            label: 'AtCoder',
                            data: graphRating,
                            fill: false,
                            lineTension: 0
                        }
                    ]
                };
            })
        }
    },
}
</script>

<style scoped>

.graphArea {
    margin: 50px auto;
    width: auto;
    max-width: 500px;
}

.others {
    margin-bottom: 70px;
}

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
.card-title {
    font-size: 20px;
    margin-bottom: 20px;
    text-align: center;
    color: #333;
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
