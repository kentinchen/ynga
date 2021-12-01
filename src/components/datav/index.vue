<template>
    <div id="data-view">
        <dv-full-screen-container>
            <div class="main-content">
                <top-header></top-header>
                <div class="main-content">
                    <left-panel class="left-panel"></left-panel>
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
        .main-content {
            flex: 1;
            display: flex;
            flex-direction: column;
        }
    }
</style>