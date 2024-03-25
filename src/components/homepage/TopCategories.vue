<script setup>
import { ref } from "vue";
import CategoriesCard from "../cards/CategoriesCard.vue";

const topCategories = ref([
  { id: 1, title: "Mobile UI Kit", count: 321, image: "categories-1.jpg" },
  { id: 2, title: "Fonts", count: 456, image: "categories-2.jpg" },
  { id: 3, title: "Icon Set", count: 789, image: "categories-3.jpg" },
  { id: 4, title: "Website UI Kit", count: 1234, image: "categories-4.jpg" },
]);
</script>

<template>
  <div class="container px-4 mx-auto my-16 md:px-12">
    <h2 class="mb-4 text-xl font-medium md:mb-0 md:text-lg">Top Categories</h2>
    <div class="flex flex-wrap -mx-1 lg:-mx-4">
      <CategoriesCard
        v-for="topCategory in topCategories"
        :key="topCategory.id"
        :title="topCategory.title"
        :count="topCategory.count"
        :image="topCategory.image"
      ></CategoriesCard>
    </div>
  </div>
</template>
