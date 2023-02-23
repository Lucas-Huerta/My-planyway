<template>
  <NuxtLayout>
    <div>
      <NuxtPage />
    </div>
  </NuxtLayout>
</template>

<style>

/* GLOBAL STYLE */
:root {
  --primary-color: #549BDE; /* bleu */
  --secondary-color: #3F292B; /* vert / noir */
  --success-color: #A8F0AD; /* vert */
  --danger-color: #DD5955; /* rouge */
}

@font-face {
  font-family: "Ginger";
  src: url("./fonts/Ginger/Ginger.ttf");
}

@font-face {
  font-family: "Raleway";
  src: url("./fonts/Raleway/Raleway-VariableFont_wght.ttf");
}

body{
  margin: 0;
}

ul{
  list-style: none;
}

a{
  text-decoration: none;
}

/* Alignement class */
.flex-row{
  display: flex;
  flex-direction: row;
}

.flex-col{
  display: flex;
  flex-direction: column;
}

/* Titles */
h1{
  font-family: "Ginger";
  font-size: 40px;
}

h2{
  font-size: 34px;
}

</style>