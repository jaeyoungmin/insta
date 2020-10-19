<template>
<transition name="component-fade" mode="out-in">
        <router-view></router-view>
        </transition>
</template>

<script>
    export default {
        name: 'View'
    }
</script>

<style lang="scss" scoped>
    .compontent-fade-enter-active, .compontent-fade-leave-active{
        transition: opacity 0.3s ease;
    }
    .compontent-fade-enter, .compontent-fade-leave-to{
        opacity: 0;
    }
</style>