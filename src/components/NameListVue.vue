<template>
    <div>
        <h3 v-for="name in names" :key="name.firstName">
            <slot :firstName="name.firstName" :lastName="name.lastName"></slot>
        </h3>
    </div>
</template>

<script>
    export default {
        name: "NameListVue",
        data() {
            return {
                names: [
                {
                    firstName: "Bruce",
                    lastName: "Wayne",
                },
                {
                    firstName: "Clark",
                    lastName: "Kent",
                },
                {
                    firstName: "Princes",
                    lastName: "Diana",
                },
            ]
            }
        }
    }
</script>

<style scoped>

</style>