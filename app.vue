<template>
   <div id="app">
      <img src="@/assets/BackImage.svg" alt="Back" id="BackImage" />
      <main>
         <NuxtLink to="/">
            <img src="@/assets/Logo.svg" alt="Necturnal Logo" />
         </NuxtLink>
         <NuxtLayout>
            <NuxtPage />
         </NuxtLayout>
      </main>
   </div>
</template>

<style >
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600&display=swap");

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

#BackImage {
   position: absolute;
   top: 0;
   left: 0;

   height: 100%;
   z-index: 0;
}
</style>