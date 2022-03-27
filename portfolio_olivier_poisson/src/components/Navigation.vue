<template>
    <div class="nav Row">
        <router-link to="/">
            <img class="logo" src="../assets/Logo.svg" alt="" />
        </router-link>
        <div class="links RowEnd">
            <div class="link">
                <router-link
                    @mouseenter="linkHover"
                    @mouseleave="linkMouseLeave"
                    to="/"
                >
                    Home
                </router-link>
                <span class="underline"></span>
            </div>
            <div class="link">
                <router-link
                    @mouseenter="linkHover"
                    @mouseleave="linkMouseLeave"
                    to="/about"
                >
                    About
                </router-link>
                <span class="underline"></span>
            </div>
        </div>
    </div>
</template>

<script>
import gsap from "gsap";
import ScrollTrigger from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);

export default {
    name: "Navigation",
    methods: {
        linkHover: function linkHover(link) {
            const target = link.target;
            const underline = target.parentElement.querySelector(".underline");
            gsap.fromTo(
                underline,
                { width: "0%" },
                { width: "100%", duration: 0.3 }
            );
            gsap.to(target, { color: "black" });
        },
        linkMouseLeave: function linkMouseLeave(link) {
            const target = link.target;
            const underline = target.parentElement.querySelector(".underline");
            gsap.to(underline, { width: "0%", duration: 0.3 });
            gsap.to(target, { color: "#1c1c1c" });
        },
        setup() {
            gsap.set(".underline", { width: "0%" });
        },
    },
};
</script>

<style scoped>
.nav {
    height: 10vh;
    position: fixed;
    width: 100vw;
    top: 0;
    z-index: 10;
    left: 0;
    background-color: rgba(0, 0, 0, 0);
    color: rgb(59, 54, 54);
    padding: 0 50px;
}
.underline {
    background: #1c1c1c;
    display: block;
    height: 3px;
    width: 0%;
}
a {
    font-size: 20px;
}
.logo {
    margin: auto 0;
    cursor: pointer;
    height: 100%;
    display: flex;
    align-items: center;
}
img {
    height: 90%;
}
.links {
    display: flex;
    width: -webkit-fill-available;
}
.link {
    margin: 0px 20px;
    cursor: pointer;
    color: rgb(34, 28, 28);
}
</style>
