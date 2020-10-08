<template>
    <div>
        <hr>
        我是子组件 
        <br>
        <Grandson></Grandson>
    </div>
</template>

<script>
    import Grandson from '../components/Grandson';
    import {EventBus} from '../eventBus';

    export default {
        components: {
            Grandson,
        }, 
        mounted () {
            //监听事件
            EventBus.$on("grandson",(msg)=>{
                console.log(msg);
            });
        },     
    }
</script>

<style scoped>

</style>