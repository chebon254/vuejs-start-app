<template>
    <div>
        <h2>Input Component</h2>
        <input type="text" :value="modelValue" @input="$emit('update:modelValue', $event.target.value)">
    </div>
</template>

<script>
    export default {
        name: "InputVue",
        props: {
            modelValue: String
        }
    }
</script>

<style scoped>

</style>