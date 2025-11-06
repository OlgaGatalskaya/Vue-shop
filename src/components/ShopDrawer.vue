<script setup>
import CartListItem from './CartListItem.vue';
import DrawerHeader from './DrawerHeader.vue';



</script>


<template>
  <div class="fixed top-0 left-0 h-full w-full bg-black z-10 opacity-70"></div>
  <div class="flex flex-col bg-white w-96 h-full fixed right-0 top-0 z-20 p-8">
    <DrawerHeader/>

    <CartListItem/>

    <div class="flex flex-col gap-3 mt-7">
        <div class="flex gap-2 ">
            <span>Total:</span>
            <div class="flex-1 border-b border-slate-300"></div>
            <b>1090 €</b>
        </div>
        <div class="flex gap-2 ">
            <span>Impuesto 21%:</span>
            <div class="flex-1 border-b border-slate-300"></div>
            <b>80 €</b>
        </div>
        <button
        disabled=""
        class="bg-lime-500 w-full rounded-xl py-3 mt-5 text-white hover:bg-lime-600 transition active:bg-lime-700 disabled:bg-slate-300 cursor-pointer">
        Comenzar pedido
    </button>
    </div>
    
  </div>
</template>
