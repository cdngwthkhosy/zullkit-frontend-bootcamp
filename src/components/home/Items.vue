<script setup>
import ItemsCard from '../card/ItemCard.vue';
import { ref } from 'vue';

const items = ref([
  {id: 1, title: 'Mobile UI Kit', category: 'Mobile UI Kit', image: '/src/assets/img/items-1.jpg'},
  {id: 2, title: 'Online Doctor Consultant', category: 'Website UI Kit', image: '/src/assets/img/items-2.jpg'},
  {id: 3, title: 'Banking Crypto', category: 'Mobile UI Kit', image: '/src/assets/img/items-3.jpg'}
])
</script>

<template>
  <div class="container px-4 mx-auto my-16 md:px-12">
    <h2 class="mb-4 text-xl font-medium md:mb-0 md:text-lg">New Items</h2>
    <div class="flex flex-wrap -mx-1 lg:-mx-4">
      <ItemsCard 
        v-for="item in items"
        :id="item.id"
        :key="item.id"
        :title="item.title"
        :category="item.category"
        :image="item.image"
      />
    </div>
  </div>
</template>