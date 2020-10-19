<template>
    <div class="main">
            <story-slider />
            <image-card />
    </div>
</template>

<script>
    export default {
        name:'Main',
        components: {
          StorySlider: () => import('@/components/main/StorySlider.vue'),
          ImageCard: () => import('@/components/main/ImageCard.vue')
        }
    }
</script>

<style lang="scss" scoped>

</style>