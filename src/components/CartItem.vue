<script setup>

    defineProps({
        imageUrl: String,
        text: String,
        price: Number,

    })
</script>


<template>
   <div class="flex  items-center gap-4 border border-slate-200 p-4 roundex-xl">
    <img class="w-16" :src="imageUrl" alt="Sneaker">
    <div class="flex flex-col ">
        <p>{{text}}</p>
        <div class="flex justify-between mt-2">
            <b>{{price}} €</b>
            <img class="opacity-40 hover:opacity-100 cursor-pointer transition" src="/close.svg" alt="Close">
        </div>
    </div>

   </div>
</template>