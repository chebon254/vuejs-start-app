<template>
    <div>
        <button @click="incrementCount">Clicked {{count}} times</button>
    </div>
</template>

<script>
import useCounter from '../composibles/useCounter'
    export default {
        name:"ClickCount",
        setup(){
            const  {count, incrementCount} = useCounter(100, 10)
            return{
                count, 
                incrementCount
            }
        }
    }
</script>

<style scoped>

</style>