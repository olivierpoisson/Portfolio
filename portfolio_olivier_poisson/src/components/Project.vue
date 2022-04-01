<template>
    <div class="container Row">
        <div class="left">
            <img :src="require(`@/assets/${imgSrc}`)" alt="background image of project" class="background" />
        </div>
        <div class="right">
            <h1 class="title">project title</h1>
            <div class="technologies Row">
                <div class="technology">
                    <img src="" alt="" />
                </div>
                <div class="technology">
                    <img src="" alt="" />
                </div>
                <div class="technology">
                    <img src="" alt="" />
                </div>
                <div class="technology">
                    <img src="" alt="" />
                </div>
            </div>
            <p class="projectDesc">project description</p>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Project",
        props: {
            imgSrc: {
                type: String,
            },
        },
    };
</script>
<style scoped>
    .container {
        margin: 0 auto;
        width: 80%;
    }
    .left {
        flex: 2;
    }
    .right {
        flex: 1;
    }
    .technologies {
        flex-wrap: wrap;
    }
    .technology > img {
        min-width: 100px;
        min-height: 100px;
    }
</style>
