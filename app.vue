<template>
   <div id="app">
      <main>
         <header class="container">
            <NuxtLink to="/" class="container-logo">
               <img src="@/assets/Logo.svg" alt="Necturnal Logo" />
            </NuxtLink>
         </header>
         <NuxtLayout>
            <NuxtPage />
         </NuxtLayout>
      </main>
   </div>
</template>

<style >
@import url("https://fonts.googleapis.com/css2?family=Abhaya+Libre:wght@700&family=Montserrat:wght@400;600&display=swap");
* {
   box-sizing: border-box;
   padding: 0;
   margin: 0;
   font-family: "Montserrat", sans-serif;
}

#app {
   height: 100vh;
   background: #f8e5d6;
   padding: 0 24px;

   background-image: url("./assets/BackImage.svg");
   background-position: left ; /* Center the image */
   background-repeat: no-repeat; /* Do not repeat the image */
   background-size: contain; /* Resize the background image to cover the entire container */

   display: flex;
   align-items: center;
   justify-content: center;
}

#app > main {
   flex: 1;
   width: 100%;
   max-width: 768px;
   margin: 0 auto;
   z-index: 2;

   display: flex;
   flex-direction: column;
   justify-content: space-evenly;
}

#app > main > *:not(a) {
   width: 100%;
}

.container {
   display: flex;
   align-items: center;
   justify-content: space-between;
   flex-wrap: wrap;
}
.container-logo {
   width: min-content;
}
.container-logo img {
   width: auto;
}
</style>