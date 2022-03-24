<template>
    <div class="nav Row">
        <router-link to="/Home">
            <img
                class="logo"
                src="../assets/undraw_Programming_re_kg9v.svg"
                alt=""
            />
        </router-link>
        <router-link to="/Home">Home</router-link>
        <router-link to="/about">About</router-link>
    </div>
</template>

<script>
export default {
    name: "Navigation",
};
</script>

<style scoped>
.logo {
    width: 100px;
    height: 50px;
}
</style>
