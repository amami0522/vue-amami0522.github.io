<template>
    <div>
        <h1>
            <font-awesome-icon icon="cog"/>
            Skill
        </h1>
        <div class="container">
            <div class="item">
                <img width="100" height="100" src="../assets/c-plusplus.svg">
                <div class="skillTitle">C++</div>
                <div class="badge-group">
                    <div class="badge-item editor">VSCode</div>
                    <div class="badge-item use">AtCoder</div>
                </div>
            </div>
            <div class="item">
                <img width="100" height="100" src="../assets/c.svg">
                <div class="skillTitle">C</div>
                <div class="badge-group">
                    <div class="badge-item editor">VSCode</div>
                    <div class="badge-item use">AtCoder</div>
                </div>
            </div>
            <div class="item">
                <img width="100" height="100" src="../assets/python.svg">
                <div class="skillTitle">Python</div>
                <div class="badge-group">
                    <div class="badge-item editor">PyCharm</div>
                    <div class="badge-item use">AtCoder</div>
                </div>
            </div>
            <div class="item">
                <img width="100" height="100" src="../assets/javascript.svg">
                <div class="skillTitle">Javascript</div>
                <div class="badge-group">
                    <div class="badge-item editor">WebStorm</div>
                    <div class="badge-item framework">Node.js</div>
                    <div class="badge-item framework">Vue.js</div>
                    <div class="badge-item framework">Deno</div>
                </div>
            </div>
            <div class="item">
                <img width="100" height="100" src="../assets/java.svg">
                <div class="skillTitle">Java</div>
                <div class="badge-group">
                    <div class="badge-item editor">Eclipse</div>
                    <div class="badge-item framework">Servlet</div>
                    <div class="badge-item framework">jsp</div>
                </div>
            </div>
            <div class="item">
                <img width="100" height="100" src="../assets/html-5.svg">
                <div class="skillTitle">HTML</div>
                <div class="badge-group">
                    <div class="badge-item editor">WebStorm</div>
                </div>
            </div>
            <div class="item">
                <img width="100" height="100" src="../assets/css-3.svg">
                <div class="skillTitle">CSS</div>
                <div class="badge-group">
                    <div class="badge-item editor">WebStorm</div>
                    <div class="badge-item framework">Bootstrap</div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "skill",
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

.badge-group {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
}

.badge-item {
    color: white;
    margin: 5px;
    padding: 5px 10px;
    border-radius: 15px;
}

.editor {
    background: #95e1d3;
}

.framework {
    background: #ff75a0;
}

.use {
    background: #fce38a;
}

.skillTitle {
    font-weight: bold;
    color: gray;
    padding: 5px;
}

</style>
