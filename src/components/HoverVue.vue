<template>
    <div>
        <h1 @mouseover="incrementCount">Clicked {{count}} times</h1>
    </div>
</template>

<script>
import CounterMixin from '../mixins/counter'
    export default {
        name: "HoverVue",
        mixins: [CounterMixin]
    }
</script>

<style scoped>

</style>