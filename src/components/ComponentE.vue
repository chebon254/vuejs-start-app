<template>
    <div>
        <h2>Component C</h2>
        <ComponentFVue/>
    </div>
</template>

<script>
import ComponentFVue from './ComponentF.vue'
    export default {
        name: "ComponentE",
        components: {
            ComponentFVue,
        }
    }
</script>

<style scoped>

</style>