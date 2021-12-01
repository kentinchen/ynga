<template>
    <div id="left-panel">
        <notice></notice>
        <status></status>
        <network></network>
    </div>
</template>

<script>
    import Notice from "./left/notice";
    import Network from "./left/network";
    import Status from "./left/status";
    export default {
        name: "leftPanel",
        components: {Status, Network, Notice},
        data() {

        },
        methods: {

        }
    }
</script>

<style lang="less">
#left-panel {
    width: 25%;
}
</style>