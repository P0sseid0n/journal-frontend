<script setup lang="ts">
defineProps<{
   label: string
}>()


</script>

<template>
   <div class="AccountInput">
      <input type="text" placeholder="&nbsp;" :id="label.replaceAll(' ', '')" />
      <label :for="label.replaceAll(' ', '')">{{ label }}</label>
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

input:not(:placeholder-shown) + label,
input:focus + label {
   color: #736d6b;

   font-size: 12px;
   top: 12px;
}

label {
   color: #834825;
   cursor: text;

   position: absolute;
   left: 0;
   top: 50%;
   transform: translateY(-50%);
   font-size: 16px;
   font-weight: 600;
   transition: all 0.15s;

   display: block;
   width: 100%;
   text-align: left;
   padding-left: 8px;
}
</style>