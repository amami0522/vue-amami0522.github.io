<template>
    <div>
        <h1>
            <font-awesome-icon icon="graduation-cap"/>
            Introduction
        </h1>
        <div class="introductionTable">
            <table class="tables">
                <tr class="tableRow">
                    <th class="tableCell">生年月日</th>
                    <td class="tableCell">2001年7月8日</td>
                </tr>
                <tr class="tableRow">
                    <th class="tableCell">所属</th>
                    <td class="tableCell">豊田工業高等専門学校</td>
                </tr>
                <tr class="tableRow">
                    <th class="tableCell">学科</th>
                    <td class="tableCell">情報工学科</td>
                </tr>
            </table>
        </div>
    </div>
</template>

<script>
export default {
    name: "introduction",
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

.introductionTable {
    color: gray;
    margin: 50px auto;
}

.tables{
    /*background-color: #CCFFFF;*/
    margin: 0 auto;
}

.tableRow {
}

.tableCell {
    padding: 30px;
}

</style>
