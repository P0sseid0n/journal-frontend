
<script setup lang="ts">

const journals = {
   'HTML': [],
   'CSS': [],
   'Java script': [],
   'Java': [],
   // 'aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa': [],
   // form => required input text
   // fazer um max-length para o texto da capa do Jornal , para não bugar o css 😆   
}

const journalsList = Object.keys(journals)

</script>

<template>
   <main>
      <div class="container-input-create">
         <input type="button" value="Criar" />
      </div>

      <div class="list" v-if="journalsList.length > 0">
         <NuxtLink v-for="(journal, i) in journalsList" :to="'/journals/' + journal">
            <img src="@/assets/Cover1.svg" alt="Journal" />
            <h3>{{ journal }}</h3>
         </NuxtLink>
      </div>
      <div class="empty" v-else>
         <img src="@/assets/EmptyState.svg" alt="EmptyState Icon" />

         <NuxtLink to="/create-journal">Criar diário</NuxtLink>
      </div>
   </main>
</template>

<style scoped>
div.list {
   display: flex;
   justify-content: space-between;
   flex-wrap: wrap;
   gap: 32px;
   padding-top: 64px;
}

.list a {
   position: relative;
   text-decoration: none;
}

.list a h3 {
   color: #000000;
   position: absolute;
   text-align: center;

   top: 50%;
   width: 100%;
   padding: 0 32px;
   transform: translateY(-50%);

   text-align: center;
   font-family: "Abhaya Libre", serif;
   font-weight: 700;
   font-size: 24px;
}

div.empty {
   display: flex;
   flex-direction: column;
   justify-content: center;
   align-items: center;
   height: 100%;
}

.empty img {
   margin-top: 128px;
   margin-bottom: 48px;
}

.empty a {
   font-weight: 600;
   font-size: 16px;

   text-decoration-line: underline;

   color: #834825;
}

.container-input-create {
   margin-top: 15px;
}
.container-input-create input {
   border: 1px solid #834825;
   color: #834825;
   background: none;
   width: 200px;
   border-radius: 24px;
   padding: 12px 16px;
   font-weight: 500;
   font-size: 16px;
}
</style>