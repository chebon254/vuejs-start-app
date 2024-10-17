<template>
    <div>
        <h2>Greeting {{name}} a.k.a {{heroName}}</h2>
    </div>
</template>

<script>
    export default {
        name: "GreetVue",
        props: ["name", "heroName"],
    }
</script>

<style scoped>

</style>