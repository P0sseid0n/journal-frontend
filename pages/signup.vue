<script setup lang="ts">

</script>

<template>
   <main>
      <header>
         <h1>Registrar</h1>
         <NuxtLink to="/signin">Já tem uma conta?</NuxtLink>
      </header>
      <AccountInput label="Defina seu nome usuário" />
      <AccountInput label="Defina sua senha" />
      <AccountInput label="Email (opcional)" />
      <button>Registrar</button>
   </main>
</template>

<style scoped>
main {
   text-align: center;
}

header {
   display: flex;
   flex-direction: row;
   justify-content: space-between;
   align-items: center;
   margin-top: 96px;
   margin-bottom: 32px;
}

h1 {
   font-weight: 400;
   font-size: 32px;

   color: #834825;
}

a {
   font-weight: 600;
   font-size: 14px;

   text-decoration-line: underline;

   color: #834825;
}

.AccountInput {
   /* margin-bottom: px; */
   margin-top: 24px;
}

button {
   cursor: pointer;
   background: #834825;
   border: 0;
   border-radius: 40px;

   font-weight: 600;
   font-size: 14px;
   color: white;

   width: 100%;
   max-width: 148px;

   height: 40px;
   margin-top: 40px;
}
</style>