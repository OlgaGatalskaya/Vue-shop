<script setup>
    import ShopCard from './ShopCard.vue';

    const onClickAdd = () => {
        alert('Add')
    }
</script>


<template>
    <div class="grid grid-cols-4 gap-5">
        <ShopCard
            imageUrl="/sneakers/sneakers-1.jpg"
            title="Zapatillas Nike Blazer Mid Suede para hombre" 
            :price="60"
            :onClickAdd="onClickAdd"
            />
    </div>
</template>
