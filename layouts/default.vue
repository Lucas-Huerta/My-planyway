<template>
    <header>
        <nav>
            <ul class="list-nav">
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
    <div>
        <slot />
    </div>
</template>

<script setup>

</script>

<style>
nav .list-nav{
    display: flex;
    flex-direction: row;
}

</style>