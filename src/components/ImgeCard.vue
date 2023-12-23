<script setup>
import { defineProps } from 'vue';
import { VHover } from 'vuetify/lib/components/index.mjs';

const { propsColor, n } =  defineProps(['isWithColor', 'n']);

const copyUrl = async(url) => {
    await navigator.clipboard.writeText(url);
}


</script>

<template>
    <VHover
    v-slot="{ isHovering, props }"
    >
    <VCard
    :elevetion="isHovering ? 12 : 2"
    v-bind="props"
    @click="copyUrl(`https://picsum.photos/500/300?image=${n * 5 + 10}${propsColor ? '' : '&grayscale'}`)"
    >
        <VImg
            :src="`https://picsum.photos/500/300?image=${n * 5 + 10}${propsColor ? '' : '&grayscale'}`"
            :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}${propsColor ? '' : '&grayscale'}`"
            aspect-ratio="1"
            cover
        >
        <template v-slot:placeholder>
          <v-row
            class="fill-height ma-0"
            align="center"
            justify="center"
          >
            <v-progress-circular
              indeterminate
              color="grey-lighten-5"
            ></v-progress-circular>
          </v-row>
        </template>
        </VImg>
    </VCard>
    </VHover>
</template>


