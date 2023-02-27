<template>
    <header>
        <nav class="main-nav">
            <ul class="list-nav flex-row">
                <NuxtLink to="/" class="nav-title">
                    My Planyway
                </NuxtLink>
                <NuxtLink to="/">
                    Accueil
                </NuxtLink>
                <NuxtLink to="/metro">
                    Métros
                </NuxtLink>
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

<style>

.main-nav{
    display: flex;
    flex-direction: row;
    align-items: center;
    background-color: var(--secondary-color);
    height: 5vh;
}

.main-nav::before{
    content: '';
    filter: blur(2rem);
    height: 100%;
    left: 0;
    position: absolute;
    top: 0;
    width: 100%;
    z-index: -1;
}

nav .list-nav{
    color: white;
    align-items: center;
    gap: 2vw;
    margin: 0;
}

nav .nav-title{
    font-family: "Ginger";
    font-size: 26px;
    margin: 0;
}

</style>