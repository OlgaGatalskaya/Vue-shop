<script setup>
import { onMounted, ref, reactive, watch } from 'vue';
import axios from 'axios';

import AppHeader from './components/AppHeader.vue'
import CardList from './components/CardList.vue'
// import ShopDrawer from './components/ShopDrawer.vue';

const items = ref([]);

const filters = reactive({
  sortBy: 'title',
  searchQuery: ''
})



const onChangeSelect = event => {
  filters.sortBy = event.target.value
  
}

const onChangeSearchInput = event => {
  filters.searchQuery = event.target.value
}

const fetchItems = async () => {
  try{
    const params = {
      sortBy: filters.sortBy,
      
    }

    console.log(params)
    if(filters.searchQuery){
      params.title = `*${filters.searchQuery}*`;
    }
    const { data } = await axios.get(
      `https://8bee9d202c309103.mokky.dev/items`,
      {
        params
      }

    )
    items.value = data

  }catch (err) {
      console.log(err)
  }
}

onMounted(fetchItems)
watch(filters, fetchItems)
</script>

<template>
  <!-- <ShopDrawer/> -->
  <div class="bg-white w-4/5 m-auto rounded-xl shadow-xl mt-14">
    <AppHeader />
    <div class="p-10">
      <div class="flex justify-between items-center">
        <h2 class="text-3xl font-bold mb-8">Todas las zapatillas</h2>
        <div class="flex gap-4">
          <select @change="onChangeSelect" class="py-2 px-3 border border-gray-200 rounded-md outline-none">
            <option value="name">Por nombre</option>
            <option value="price">Por precio (baratos)</option>
            <option value="-price">Por precio (caros)</option>
          </select>
          <div class="relative">
            <img class="absolute left-4 top-3" src="/search.svg" alt="" />
            <input
              @input="onChangeSearchInput"
              placeholder="Buscar..."
              class="border border-gray-200 rounded-md py-2 pl-11 pr-4 outline-none focus:border-gray-400"
              type="text"
            />
          </div>
        </div>
      </div>
      <div class="mt-10"></div>
      <CardList :items="items"/>
    </div>
  </div>
</template>
