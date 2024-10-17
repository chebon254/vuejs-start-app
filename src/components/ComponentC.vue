<template>
    <div>
        <h2>Component C</h2>
        <ComponentEVue/>
    </div>
</template>

<script>
import ComponentEVue from './ComponentE.vue'
    export default {
        name: "ComponentC",
        components: {
            ComponentEVue,
        }
    }
</script>

<style scoped>

</style>