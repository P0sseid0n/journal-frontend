<script setup lang="ts">
const route = useRoute()
console.log(route)

const notes = [
   'The h1, h2, h3, h4, h5, and h6 elements',
   'The article element',
]

</script>

<template>
   <header v-if="notes.length > 0">
      <NuxtLink class="back" :to="(route.params.journal as string)">
         <img src="@/assets/ArrowLeft.svg" alt="Back Icon" />
         {{ route.params.journal }}
      </NuxtLink>
      <NuxtLink class="add" to="/create-note">
         <img src="@/assets/Add.svg" alt="Add Icon" />
         Adicionar nota
      </NuxtLink>
   </header>
   <div class="list" v-if="notes.length > 0">
      <NuxtLink v-for="(note, i) in notes" :to="'/journals/' + route.params.journal + '/' + note">
         <img src="@/assets/Article.svg" alt="Journal" />
         <h5>{{ note }}</h5>
      </NuxtLink>
   </div>
   <div class="empty" v-else>
      <p>{{ route.params.journal }}</p>
      <img src="@/assets/EmptyState.svg" alt="EmptyState Icon" />

      <NuxtLink to="/create-note">Criar nota</NuxtLink>
   </div>
</template>



<style scoped>
header {
   display: flex;
   justify-content: space-between;
   align-items: center;
   margin-top: 32px;
}

header a {
   color: #000;
   text-decoration: none;
}
header .back {
   font-family: "Abhaya Libre";
   font-weight: 700;
   font-size: 20px;

   display: flex;
   flex-direction: row;
   align-items: center;
}

header .add {
   border: 1px solid #834825;
   color: #834825;
   border-radius: 24px;
   padding: 12px 16px;
   font-weight: 500;
   font-size: 16px;
}
div.list {
   display: flex;
   justify-content: center;
   flex-wrap: wrap;
   padding-top: 16px;
   gap: 16px;
}
div.list a {
   position: relative;
   text-decoration: none;
}

div.list h5 {
   color: #000;
   font-weight: 400;
   font-size: 20px;
   text-overflow: ellipsis;
   overflow: hidden;

   position: absolute;
   left: 0;
   top: 0;

   width: 100%;
   height: 100%;

   padding: 24px 32px;
   padding-bottom: 32px;
}
div.empty {
   display: flex;
   flex-direction: column;
   justify-content: center;
   align-items: center;
   height: 100%;
   padding-top: 64px;
}

.empty p {
   font-size: 24px;
   font-weight: bold;
   font-family: "Abhaya Libre", serif;
   margin-bottom: 64px;
}

.empty img {
   margin-bottom: 48px;
}

.empty a {
   font-weight: 600;
   font-size: 16px;

   text-decoration-line: underline;

   color: #834825;
}
</style>