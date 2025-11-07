<script setup>
import AppHeader from './components/AppHeader.vue'
import CardList from './components/CardList.vue'
// import ShopDrawer from './components/ShopDrawer.vue';
</script>

<template>
  <!-- <ShopDrawer/> -->
  <div class="bg-white w-4/5 m-auto rounded-xl shadow-xl mt-14">
    <AppHeader />
    <div class="p-10">
      <div class="flex justify-between items-center">
        <h2 class="text-3xl font-bold mb-8">Todas las zapatillas</h2>
        <div class="flex gap-4">
          <select class="py-2 px-3 border border-gray-200 rounded-md outline-none">
            <option value="">Por nombre</option>
            <option>Por precio (baratos)</option>
            <option>Por precio (caros)</option>
          </select>
          <div class="relative">
            <img class="absolute left-4 top-3" src="/search.svg" alt="" />
            <input
              placeholder="Buscar..."
              class="border border-gray-200 rounded-md py-2 pl-11 pr-4 outline-none focus:border-gray-400"
              type="text"
            />
          </div>
        </div>
      </div>
      <CardList />
    </div>
  </div>
</template>
