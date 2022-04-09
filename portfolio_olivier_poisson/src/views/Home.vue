<template>
    <section class="hero">
        <div class="web">
            <h1 class="titleWeb">Web</h1>
            <p class="text">I love to help compagnies build amazing and attracting websites that help them get more customers</p>
        </div>
        <img class="heroImg" src="../assets/Heroimage.png" alt="" />
        <div class="software">
            <h1 class="titleSoft">Software</h1>
            <p class="text">
                I love to help compagnies build amazing and functionnal softwares so they can give their customers the best experience possible
            </p>
        </div>
    </section>
    <section class="section2">
        <div class="Project" v-for="project in projects" v-bind:key="project.id">
            <Project :title="project.title" :imgSrc="project.image" />
        </div>
    </section>
</template>

<script>
    import gsap from "gsap";
    import ScrollTrigger from "gsap/ScrollTrigger";
    import Project from "../components/Project.vue";
    gsap.registerPlugin(ScrollTrigger);

    export default {
        name: "Home",
        data() {
            return {
                projects: [
                    {
                        id: 1,
                        title: "Film Apis",
                        image: "FilmApis1.png",
                        description: "Website used to view and search information about movies, actors",
                    },
                ],
            };
        },
        components: {
            Project: Project,
        },
        methods: {
            heroScrollAnimation() {
                const timeline = gsap.timeline({
                    scrollTrigger: {
                        trigger: ".hero",
                        start: "0%",
                        end: "80%",
                        scrub: true,
                    },
                });
                timeline.fromTo(".hero", { opacity: 1 }, { opacity: 0 });
            },
            HeroTextAnimation() {
                const timeline = gsap.timeline({
                    defaults: {
                        duration: 1,
                    },
                });
                timeline.fromTo(".heroImg", { opacity: 0 }, { opacity: 1, duration: 2, ease: "Power2.easeIn" });
                timeline.fromTo(".titleWeb", { x: 50, opacity: 0 }, { x: 0, opacity: 1, ease: "Power2.easeOut" }, "<50%");
                timeline.fromTo(".titleSoft", { x: -50, opacity: 0 }, { x: 0, opacity: 1, ease: "Power2.easeOut" }, "<");
                timeline.fromTo(".text", { y: 50, opacity: 0 }, { y: 0, opacity: 1 }, "<50%");
            },
            setup() {
                gsap.set(".underline", { width: "0%" });
                gsap.set(".hero", { zIndex: "-1" });
                gsap.set(".section2", { zIndex: "2", position: "relative" });
            },
        },
        mounted: function () {
            this.heroScrollAnimation();
            this.HeroTextAnimation();
        },
    };
</script>
<style scoped>
    .hero {
        height: 100vh;
        display: flex;
        z-index: 1;
        justify-content: center;
        position: sticky;
        top: 0;
    }
    .heroImg {
        transform: scale(1.3);
        transform-origin: bottom;
    }

    .web,
    .software {
        display: flex;
        align-items: center;
        flex: 1;
        flex-direction: column;
        padding: 0px 50px;
        justify-content: center;
        overflow: hidden;
    }
    .titleWeb,
    .titleSoft {
        font-size: 4em;
    }
    .section2 {
        z-index: 2;
        padding: 10vw;
        position: relative;
    }
    .text {
        color: #4d4b4b;
    }
</style>
