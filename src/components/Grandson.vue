<template>
    <div>
        <hr>
        我是孙子组件
        <br>
        <button @click="handleMsg">点击发出消息</button>
    </div>
</template>

<script>
    import {EventBus} from '../eventBus';
    export default {
        methods: {
            handleMsg() {
                //发出grandson事件
                EventBus.$emit("grandson","我是组件GrandSon")
            }
        },
    }
</script>

<style scoped>

</style>