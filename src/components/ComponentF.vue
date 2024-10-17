<template>
    <div>
        <h1>Component F</h1>
        <h3>Component F {{username}}</h3>
    </div>
</template>

<script>
    export default {
        name: "ComponentF",
        inject: ["username"]
    }
</script>

<style scoped>

</style>