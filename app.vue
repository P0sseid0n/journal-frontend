<template>
   <div id="app">
      <img src="@/assets/BackImage.svg" alt="Back" id="BackImage" />
      <img src="@/assets/Logo.svg" alt="Necturnal Logo" />
      <NuxtLayout>
         <NuxtPage />
      </NuxtLayout>
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
   flex-direction: column;
   justify-content: center;
   align-items: flex-start;
}

#app > *:not(img) {
   z-index: 2;
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