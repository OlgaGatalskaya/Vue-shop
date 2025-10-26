<script setup>
import AppHeader from './components/AppHeader.vue';
import ShopCard from './components/ShopCard.vue';

</script>

<template>
  <div class="bg-white w-4/5  m-auto rounded-xl shadow-xl mt-14">
    <AppHeader/>
    <div class="p-10">
      <h2 class="text-3xl font-bold mb-8">Todas las zapatillas</h2>

      <div class="grid grid-cols-4 gap-5">
        <ShopCard/>
        <ShopCard/>
        <ShopCard/>
        <ShopCard/>
        <ShopCard/>
      </div>
    </div>
    
  </div>
</template>
