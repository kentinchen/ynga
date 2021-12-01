<template>
    <div id="right-panel">
        <product></product>
    </div>
</template>

<script>
    import Product from "./right/product";
    export default {
        name: "rightPanel",
        components: {Product}
    }
</script>

<style lang="less">
#right-panel{
    width: 25%;
}
</style>