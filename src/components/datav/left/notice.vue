<template>
    <div id="notice">
        <div>公告</div>
        <div class="small">
            <div>平台累计运行天数：{{runtime}}天 当日重要通告数：<span class="small-red">{{count}}</span>条</div>
        </div>
        <dv-scroll-board :config="config"/>
    </div>
</template>

<script>
    export default {
        name: "notice",
        data() {
            return {
                count: 0,
                runtime: 0,
                config: {
                    header: ['No','通告标题'],
                    data: [
                        ['1','WJ运营大屏重要公告标题'],
                        ['2','全市深入推进党史学习教育“民呼我为”主题活动部署会召开'],
                        ['3','周江勇赴西溪湿地调研'],
                        ['4','杭州市人民政府 关于调整杭州市部分行政区划的通知'],
                        ['5','周江勇主持召开城市地下隐患专项治理工作专题会议']
                    ],
                    index: false,
                    columnWidth: [50,300],
                    align: ['left'],
                    rowNum: 4,
                    headerBGC: '#1981f6',
                    headerHeight: 16,
                    oddRowBGC: 'rgba(0, 44, 81, 0.8)',
                    evenRowBGC: 'rgba(10, 29, 50, 0.8)'
                }
            }
        },
        methods: {
            getNotice (){
                this.count = 5;
                this.runtime = 232;
            }
        },
        mounted() {
            const { getNotice } = this

            getNotice()

            setInterval(this.getNotice, 30000)
        }
    }
</script>

<style lang="less">
    #notice {
        width: 100%;
        background-image: url("//datav.oss-cn-hangzhou.aliyuncs.com/uploads/images/5f96c0a7bdc919b2d8286c0bb71587cb.png");

        .small {
            font-size: 12px;
        }

        .small-red {
            color: rgba(255, 0, 0);
            font-size: 12px;
        }
    }
</style>