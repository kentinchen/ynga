<template>
    <div id="data-view">
        <dv-full-screen-container>
            <div class="main-content">
                <top-header></top-header>
                <div class="block-left-right-content">
                    <left-panel></left-panel>
                    <center-panel></center-panel>
                    <right-panel></right-panel>
                </div>
            </div>
        </dv-full-screen-container>
    </div>
</template>

<script>
    import topHeader from "./topHeader";
    import LeftPanel from "./leftPanel";
    import CenterPanel from "./centerPanel";
    import RightPanel from "./rightPanel";

    export default {
        name: "DataView",
        components: {
            RightPanel,
            CenterPanel,
            LeftPanel,
            topHeader
        },
        data() {
            return {}
        },
        methods: {}
    }
</script>

<style lang="less">
    #data-view {
        pointer-events: auto;
        background-repeat: no-repeat;
        background-size: 100% 100%;
        background-image: url("https://xunmi777.oss-cn-shanghai.aliyuncs.com/flare%2001.jpg");
        cursor: default;

        #dv-full-screen-container {
            background-image: url('./image/bg.png');
        }

        .main-content {
            flex: 1;
            display: flex;
            flex-direction: column;
        }

        .block-left-right-content {
            flex: 1;
            display: flex;
            margin-top: 20px;
        }
    }
</style>