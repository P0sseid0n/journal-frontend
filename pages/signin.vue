<script setup lang="ts">
const router = useRouter()

function signin() {
   router.push('/journals')
}

</script>

<template>
   <main>
      <header>
         <h1>Entrar</h1>
         <NuxtLink to="/signup">Criar conta</NuxtLink>
      </header>
      <AccountInput label="Seu nome de usuário" />
      <AccountInput label="Sua senha" />
      <footer>
         <a href="/">Esqueceu a senha?</a>
      </footer>
      <button @click="signin">Entrar</button>
   </main>
</template>

<style scoped>
main {
   text-align: center;
}

main > footer {
   text-align: right;
   margin-bottom: 40px;
   margin-top: 16px;
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
}
</style>