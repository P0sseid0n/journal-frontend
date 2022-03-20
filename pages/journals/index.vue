<script setup lang="ts">

const journals = {
   'HTML': [],
   'CSS': [],
   'Java script': [],
}

const journalsList = Object.keys(journals)

</script>

<template>
   <main>
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
   justify-content: center;
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
</style>