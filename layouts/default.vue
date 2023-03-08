<template>
    <header>
        <nav class="main-nav" ref="mainNav">
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

<script setup>

let route = useRoute(); 
let mainNav = ref(null);

onUpdated(() =>{
  if (route.fullPath == "/") {
    mainNav.value.classList.remove('backgound-nav');
  }
  else{
    mainNav.value.classList.remove('backgound-nav');
  }
})

</script>

<style>

.main-nav{
    position: absolute;
    z-index: 10;
    width: 100vw;
    display: flex;
    flex-direction: row;
    align-items: center;
    height: 7vh;
    background: rgba(255, 255, 255, 0.07);
    /* border-radius: 16px; */
    box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
    backdrop-filter: blur(3.8px);
    -webkit-backdrop-filter: blur(3.8px);
    /* border: 1px solid rgba(255, 255, 255, 0.74); */
}

.backgound-nav{
    background-color: #170C08;
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