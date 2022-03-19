<script setup lang="ts">
defineProps<{
   label: string
}>()
</script>

<template>
   <div class="AccountInput">
      <input type="text" placeholder="&nbsp;" />
      <span>{{ label }}</span>
   </div>
</template>



<style scoped>
div {
   background: #fff;
   position: relative;
   height: 56px;
   width: 100%;
}

input {
   width: 100%;
   height: 100%;
   background: transparent;
   border: none;
   outline: none;
   font-size: 16px;
   padding: 0 8px;
   padding-top: 16px;
   color: #834825;
}

input:not(:placeholder-shown) + span,
input:focus + span {
   color: #736d6b;

   transform: translateY(0%) scale(0.75);
   top: 4px;
   left: 0px;
}

/* input:not(:placeholder-shown) + span {
   transform: translateY(0%) scale(0.75);
   top: 4px;
} */

span {
   color: #834825;

   position: absolute;
   left: 8px;
   top: 50%;
   transform: translateY(-50%);
   font-size: 16px;
   font-weight: 600;
   transition: all 0.2s;
}
</style>