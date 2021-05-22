<template>
    <div>
        <template>
            <v-tabs :value="3" background-color="primary">
                <v-tab @click="$router.push({name:'Case'})">用例管理</v-tab>
                <v-tab @click="$router.push({name:'Task'})">任务管理</v-tab>
                <v-tab @click="$router.push({name:'Jenkins'})">Jenkins管理</v-tab>
                <v-tab @click="$router.push({name:'Report'})">报告管理</v-tab>
            </v-tabs>
        </template>
        <div id="main" style="width:500px;height:500px"></div>
        report</div>
    
</template>

<script>
export default {
    data() {
        return {

        }
    },
    methods: {
        
    },
    mounted(){
        var echarts = require('echarts');
        var myChart = echarts.init(document.getElementById('main'));
        myChart.setOption({
            title:{
                text:'Echarts 入门展示'
            },
            tooltip:{},
            xAxis:{
                data:['衬衫','羊毛衫','雪容山','裤子','高跟鞋','袜子']
            },
            yAxis:{},
            series:[{
                name:'销量',
                type:'bar',
                data:[5,20,36,10,10,20]
            }]
            
        });
    },

}

</script>
<style scoped>

</style>