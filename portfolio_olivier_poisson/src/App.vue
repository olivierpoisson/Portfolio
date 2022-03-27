<template>
    <Navigation />
    <router-view />
</template>

<script>
import Navigation from "./components/Navigation.vue";

export default {
    components: {
        Navigation,
    },
};
</script>

<style>
* {
    font-family: "DM Sans", sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
#app {
    min-height: 100vh;
    color: rgb(255, 255, 255);
    line-height: 1.5;
    background: #ece9e6; /* fallback for old browsers */
    background: -webkit-linear-gradient(
        to top,
        #ffffff,
        #ece9e6
    ); /* Chrome 10-25, Safari 5.1-6 */
    background: linear-gradient(to top, #ffffff, #ece9e6);
    scroll-behavior: smooth;
}

button {
    padding: 1em 2em;
}
button:active {
    transform: scale(0.95);
}
a,
p {
    text-decoration: none;
    color: #1f1c1c;
}
h1,
h2,
h3,
h4,
h5,
a,
p {
    text-underline-offset: 5px;
    color: #1f1c1c;
}
.Row {
    display: flex;
}
.RowCenter {
    display: flex;
    align-items: center;
    justify-content: center;
}
.RowEnd {
    display: flex;
    align-items: center;
    justify-content: flex-end;
}
.Col {
    display: flex;
    flex-direction: column;
}
.ColCenter {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}
</style>
