<script setup>
    import ShopCard from './ShopCard.vue';

    defineProps({
        items: Array
    })

    const onClickAdd = () => {
        alert('Add')
    }
</script>


<template>
    <div class="grid grid-cols-4 gap-5">
        <ShopCard
            v-for="item in items"
            :key = "item.id"
            :imageUrl="item.imageUrl"
            :title="item.title" 
            :price="item.price"
            :onClickAdd="onClickAdd"
            />
    </div>
</template>
