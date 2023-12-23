<script setup>
import ImgeCard from './ImgeCard.vue';
</script>

<template>
    <VCard class="mx-5 my-2 pa-3" >
    <VRow>
      <VCol
        v-for="n in 200"
        :key="n"
        cols="4"
        sm="3"
        md="2"
        lg="1"
      >
        <ImgeCard :n="n"  />
      </VCol>
    </VRow>
  </VCard>
</template>
