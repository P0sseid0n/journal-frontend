<script setup lang="ts">
const route = useRoute()

</script>

<template>
   <main>
      <header>
         <NuxtLink class="back" :to="'/journals/' + encodeURI(route.params.journal as string)">
            <img src="@/assets/ArrowLeft.svg" alt="Back Icon" />
            {{ route.params.journal }}
         </NuxtLink>
      </header>
      <form @submit.prevent class="container-form">
         <input type="text" placeholder="Titulo" required maxlength="30" />
         <textarea placeholder="Escreva sua nota" required maxlength="100"></textarea>
         <button>Salvar nota</button>
      </form>
   </main>
</template>



<style scoped>
main {
   display: flex;
   flex-direction: column;
   align-items: center;
   gap: 32px;
   padding-top: 48px;
}

header {
   width: 100%;
}

header a {
   color: #000;
   text-decoration: none;
   font-family: "Abhaya Libre";
   font-weight: 700;
   font-size: 20px;

   display: flex;
   flex-direction: row;
   align-items: center;
}

input,
textarea {
   width: 100%;
   background: rgba(255, 255, 255, 0.42);
   border: 1px solid rgba(157, 164, 166, 0.07);
   border-radius: 4px;
   resize: none;

   color: #804627;
   font-weight: 600;
   font-size: 14px;

   padding: 16px 12px;
}

textarea {
   height: 300px;
   margin: 0 auto;
   margin-bottom: 8px;
}

input::placeholder,
textarea::placeholder {
   color: #804627;
   font-weight: 600;
   font-size: 14px;
}

button {
   border: none;
   color: #fff;
   font-weight: 600;
   font-size: 14px;
   background: #834825;
   border-radius: 24px;
   cursor: pointer;

   height: 40px;
   width: 100%;
   max-width: 190px;
}
.container-form {
   width: 100%;
   display: flex;
   align-items: center;
   justify-content: space-around;
   flex-direction: column;
}
.container-form input {
   margin: 5px;
}
</style>