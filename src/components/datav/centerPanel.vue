<template>
    <div id="center-panel">
        <business></business>
        <business-map></business-map>
    </div>
</template>

<script>
    import Business from "./center/business";
    import BusinessMap from "./center/businessMap";
    export default {
        name: "centerPanel",
        components: {BusinessMap, Business}
    }
</script>

<style lang="less">
#center-panel {
    width: 50%;
}
</style>