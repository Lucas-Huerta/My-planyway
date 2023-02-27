<template>
    <header>
        <nav>
            <ul class="list-nav flex-row">
                <h1 class="nav-title">
                    My Planyway
                </h1>
                <li>
                    Accueil
                </li>
                <li>
                    Métros
                </li>
                <li>
                    RER
                </li>
                <li>
                    À propos
                </li>
            </ul>
        </nav>
    </header>
    <slot />
</template>

<script setup>

</script>

<style>
nav .list-nav{
    color: white;
    align-items: center;
    gap: 2vw;
}

nav .nav-title{
    font-size: 26px;
    margin: 0;
}

</style>