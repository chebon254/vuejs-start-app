<template>
    <div>
        <h2>Popup</h2>
        <button @click="$emit('close', 'Kibet')">Close Popup</button>
    </div>
</template>

<script>
    export default {
        name: "PopupVue",
        emits: ["close"]
    }
</script>

<style scoped>

</style>