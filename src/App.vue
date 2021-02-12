<template>
    <div id="app">
        <div class="container grid-lg">
            <header class="navbar">
                <section class="navbar-section">
                    <router-link to="/" class="btn btn-link">Home</router-link>
                    <router-link to="/kanban" class="btn btn-link">Kanban</router-link>
                </section>
                <section class="navbar-center">
                    <img class="img-responsive img-logo" src="@/assets/logo.png" alt="logomarcar tdlst">
                </section>
                <section class="navbar-section">
                    <a href="" class="btn btn-link">Twiter</a>
                    <a href="" class="btn btn-link">GitHub</a>
                </section>
            </header>
            <router-view> </router-view>
        </div>
    </div>
</template>

<style scoped>
.img-logo {
    max-width: 125px;
}
</style>