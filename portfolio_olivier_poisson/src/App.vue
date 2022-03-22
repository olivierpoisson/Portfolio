<template>
    <div id="nav">
        <img src="assets/images/Portfolio_Logo.png" alt="" />
        <img src="assets/logo.png" alt="" />
        <router-link to="/"
            ><img src="assets/images/Portfolio_Logo.png" alt=""
        /></router-link>
        <router-link to="/">Home</router-link>
        <router-link to="/about">About</router-link>
    </div>
    <router-view />
</template>

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

#nav a.router-link-exact-active {
}
</style>
