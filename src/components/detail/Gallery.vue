<script setup>
import { ref } from "vue";

const defaultImage = ref("/src/assets/img/gallery-3.png");
const galleries = ref([
  { id: 1, image: "/src/assets/img/gallery-2.png" },
  { id: 2, image: "/src/assets/img/gallery-3.png" },
  { id: 3, image: "/src/assets/img/gallery-4.png" },
  { id: 4, image: "/src/assets/img/gallery-5.png" },
]);

function changeImage (image) {
  this.defaultImage = image
}
</script>

<template>
  <section id="gallery">
    <img :src="defaultImage" alt="" class="w-full mt-6 rounded-2xl" />
    <div class="grid grid-cols-4 gap-4 mt-4">
      <template v-for="gallery in galleries" :key="gallery.id">
        <div
          @click="changeImage(gallery.image)"
          class="overflow-hidden cursor-pointer rounded-2xl"
          :class="{ 'ring-2 ring-indigo-500': defaultImage == gallery.image }"
        >
          <img :src="gallery.image" class="w-full" alt="" />
        </div>
      </template>
    </div>
  </section>
</template>
