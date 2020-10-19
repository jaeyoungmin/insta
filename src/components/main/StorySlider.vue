<template>
    <div class="story-slider">
        <div class="wrapper">
            <div class="story-item">
                <v-badge bordered color="blue" bottom overlap icon="mdi-plus"
                offset-x="20" offset-y="20">
                    <img :src="myProfile.img" alt="#" contain />
                </v-badge>
                <p>내 스토리</p>
            </div>
            <div class="story-item"  v-for="(story, i) in stories" :key="i">
                <img :src="story.img" alt="#" contain />     
                <p>{{story.name}}</p>
            </div>
            <!-- /.story-item -->
        </div>
        <!-- /.wrapper -->
    </div>
</template>

<script>
import {mapState} from 'vuex'
    export default {
        name: 'StorySlider',
        computed: { ...mapState(["stories", "myProfile"]) }
        //변경안함
    }
</script>

<style lang="scss" scoped>
.story-slider{
    overflow-x: auto;
    background-color: #fafafa;
    border-bottom:1px solid #8080807a;
}
.wrapper{
    padding:10px 10px 0;
    white-space: nowrap;
}
.story-item{
    width:100px;
    height:100px;
    display:inline-block;
    margin-right:10px;
    text-align: center;
    img{
        width:80px;
        height:80px;
        border-radius: 50%;
        object-fit: cover;
        vertical-align: middle;
        
    }
    p{
        font-size:12px;
        padding: 0;
        margin:0;
    }
}

</style>