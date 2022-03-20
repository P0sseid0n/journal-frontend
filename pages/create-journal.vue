<script setup lang="ts">
const name = ref('')
const router = useRouter()

function createJournal() {
   if (name.value.trim().length == 0) return

   router.push('/')
}

</script>

<template>
   <main>
      <div>
         <img src="@/assets/BookCreate.svg" alt="Book" />
         <h3 v-text="name"></h3>
      </div>
      <input type="text" v-model="name" />
      <button @click="createJournal">Criar diário</button>
   </main>
</template>



<style scoped>
main {
   margin-top: 96px;
   display: flex;
   flex-direction: column;
   justify-content: center;
   align-items: center;
   height: 100%;
}

div {
   position: relative;
}

h3 {
   position: absolute;
   top: 50%;
   width: 100%;
   padding: 0 40px;

   word-wrap: break-word;
   text-align: center;
   font-family: "Abhaya Libre", serif;
   font-weight: 700;
   font-size: 24px;

   transform: translateY(-50%);
}
input {
   margin-top: 32px;
   margin-bottom: 40px;
   padding: 0 16px;

   width: 100%;
   height: 40px;

   background: rgba(255, 255, 255, 0.42);
   border: 1px solid rgba(157, 164, 166, 0.07);
   border-radius: 4px;

   font-weight: 600;
   font-size: 16px;

   color: #804627;

   max-width: 320px;
}

button {
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