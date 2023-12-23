<script setup>
import Sidebar from './components/Sidebar.vue';
import Gallery from './components/Gallery.vue';
import {ref} from 'vue';

const isWithColor = ref(true)

const onSelectOption = (isColor) => {
  isWithColor.value = isColor;
}
</script>

<template>
  <VApp>
    <Sidebar 
    @selectOption="onSelectOption"
    />
    <VMain>
      <Gallery :isWithColor="isWithColor"/>
    </VMain>
  </VApp>
</template>



