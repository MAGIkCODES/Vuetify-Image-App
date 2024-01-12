<script setup>
  import sideBar from '@/components/sideBar.vue'
  import ImageGallery from './components/ImageGallery.vue';
  import{ ref } from 'vue'

  const isWithColor = ref(true)
  const onSelectOption = (isColor) => {
    isWithColor.value = isColor
  }
</script>

<template>
  <v-app>
   <sideBar @selectOption="onSelectOption" />
    <v-main>
      <ImageGallery :isWithColor="isWithColor" />
    </v-main>
  </v-app>
</template>


