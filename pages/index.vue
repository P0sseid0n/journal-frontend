<script setup lang="ts">

</script>

<template>
   <div class="container">
      <h1>Olá</h1>
      <NuxtLink to="/signin">
         <input class="input-button-next" type="button" value=" Entrar" />
      </NuxtLink>
   </div>
</template>

<style scoped>
.container {
   display: flex;
   align-items: center;
   flex-direction: column;
   
 
}
h1 {
   margin-top: 15px;
   margin-right: auto;
}
.input-button-next {
   margin-top: 20px;
   border: none;
   color: #ffffff;
   background: #834825;
   border-radius: 24px;

   width: 196px;
   height: 40px;

   font-weight: 600;
   font-size: 14px;

   cursor: pointer;
}
</style>