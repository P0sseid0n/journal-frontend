<script setup lang="ts">

</script>

<template>
   <main>
      <img src="@/assets/EmptyState.svg" alt="EmptyState Icon" />

      <NuxtLink to="/create-journal">Criar diário</NuxtLink>
   </main>
</template>

<style scoped>
main {
   display: flex;
   flex-direction: column;
   justify-content: center;
   align-items: center;
   height: 100%;
}

img {
   margin-top: 128px;
   margin-bottom: 48px;
}

a {
   font-weight: 600;
   font-size: 16px;

   text-decoration-line: underline;

   color: #834825;
}
</style>