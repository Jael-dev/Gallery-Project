<script setup>
import { defineEmits } from 'vue';
const emits = defineEmits(['selectOption']);

const selectOption = (isWithColor) => {
    emits("selectOption", isWithColor);
}
</script>

<template>
    <VNavigationDrawer
    expand-on-hover
    rail
    >
    <VList>
          <VListItem
            prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg"
            title="Jael Kalvin"
            subtitle="jaelngaleu@gmailcom"
          ></VListItem>
        </VList>

        <v-divider></v-divider>

        <VList density="compact" nav>
          <VListItem prepend-icon="mdi-image" 
          title="Color Gallery" 
          value="color" 
          @click="selectOption(true)"
          ></VListItem>
          <VListItem prepend-icon="mdi-dialpad" title="Grey Gallery" value="grey" @click="selectOption(false)"></VListItem>
        </VList>
    </VNavigationDrawer>
</template>


