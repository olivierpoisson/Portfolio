<template>
    <div class="container Row">
        <div class="left">
            <img :src="require(`@/assets/${imgSrc}`)" alt="background image of project" class="background" />
        </div>
        <div class="right">
            <h1 class="title">{{ title }}</h1>
            <h3 class="subtitle">Technologies used</h3>
            <div class="technologies Row">
                <div v-for="tech in technologies" :key="tech" class="technology">
                    <img class="techImg" :src="require(`@/assets/${tech.imgSrc}`)" :alt="tech.Name" />
                    <p>{{ tech.Name }}</p>
                </div>
            </div>
            <p class="projectDesc">project description</p>
            <div class="RowCenter">
                <button @click="triggerFullScreen" class="viewMore">{{ fullScreen ? "View Less" : "View More" }}</button>
            </div>
        </div>
    </div>
</template>

<script>
    import gsap from "gsap";
    const timeline = gsap.timeline({
        defaults: {
            duration: 1,
            ease: "Power2.easeOut",
        },
    });
    export default {
        name: "Project",
        props: {
            imgSrc: {
                type: String,
            },
            title: { type: String },
            technologies: { type: [] },
        },
        data() {
            return {
                fullScreen: false,
            };
        },
        methods: {
            triggerFullScreen() {
                if (!this.fullScreen) {
                    timeline.to(".container", { height: "100vh" });
                    timeline.to("body", { overflowY: "hidden" }, "<");
                    timeline.to(
                        ".section2",
                        {
                            zIndex: 10,
                            padding: 0,
                        },
                        "<"
                    );
                    timeline.to(".left", { height: "100%" }, "<");
                    timeline.to(".right", { height: "100%" }, "<");
                }
                this.fullScreen = !this.fullScreen;
            },
        },
    };
</script>
<style scoped>
    .container {
        margin: 0 auto;
        height: 80vh;
        width: 100%;
        transform-origin: center;
    }
    .left {
        flex: 2;
        transform-origin: center;
    }
    .right {
        flex: 1;
        transform-origin: center;
    }
    .technologies {
        flex-wrap: wrap;
        padding: 10px 0px;
    }
    .technology > img {
        min-width: 100px;
        min-height: 100px;
        width: 100%;
    }
    .technology > p {
        text-align: center;
    }
    .title {
        text-align: center;
        font-size: 2.5em;
    }
    .subtitle {
        text-align: center;
    }
    .projectDesc {
        font-size: 1.5em;
    }
    .background {
        width: 100%;
        height: 100%;
        border-radius: 20px 0px 0px 20px;
    }
    .technology {
        width: min-content;
    }
</style>
