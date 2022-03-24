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
#app {
    color: #2c3e50;
}

#nav {
    padding: 30px;
}

#nav a {
    font-weight: bold;
    color: #2c3e50;
}
Row {
    display: flex;
}
.RowCenter {
    display: flex;
    align-items: center;
    justify-content: center;
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
button {
    padding: 1em 2em;
}
button:active {
    transform: scale(0.95);
}
a {
    text-decoration: none;
    color: #2c3e50;
}
h1,
h2,
h3,
h4,
h5,
a,
p {
    text-underline-offset: 5px;
}
</style>
