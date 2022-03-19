<template>
   <div id="app">
      <img src="@/assets/BackImage.svg" alt="Back" id="BackImage" />
      <div>
         <img src="@/assets/Logo.svg" alt="Necturnal Logo" />
      </div>
      <NuxtLayout>
         <NuxtPage />
      </NuxtLayout>
   </div>
</template>

<style>
* {
   box-sizing: border-box;
   padding: 0;
   margin: 0;
}
#app {
   height: 100vh;
   background: #f8e5d6;

   display: flex;
   flex-direction: column;
   justify-content: center;
}

#BackImage {
   position: absolute;
   top: 0;
   left: 0;

   height: 100%;
}
</style>