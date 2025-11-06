<script setup>
import AppHeader from './components/AppHeader.vue';
import CardList from './components/CardList.vue';
import ShopDrawer from './components/ShopDrawer.vue';
</script>

<template>
  <ShopDrawer/>
  <div class="bg-white w-4/5  m-auto rounded-xl shadow-xl mt-14">
    <AppHeader/>
    <div class="p-10">
      <h2 class="text-3xl font-bold mb-8">Todas las zapatillas</h2>
      <CardList/>
      
    </div>
    
  </div>
</template>
