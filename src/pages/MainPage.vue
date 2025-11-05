<template>
  <q-layout>
    <div class="no-shadow bg-transparent absolute-top z-max">
      <q-toolbar class="row items-center">
        <q-btn dense flat round icon="menu" @click="toggleLeftDrawer" color="white" />
        <q-toolbar-title>
          <div class="column items-center justify-start">
            <h2 class="text-h2 q-mb-none q-mt-lg text-light-blue-7 playfair-display cursor-pointer">
              ZHETIJER
            </h2>
            <h6 class="text-h6 text-yellow-9 playfair-display q-ma-none q-mb-sm">
              Qazaqstannyń jeti ǵazhaiyby
            </h6>
          </div>
        </q-toolbar-title>
      </q-toolbar>
    </div>
    <q-drawer show-if-above overlay v-model="leftDrawerOpen" side="left"> </q-drawer>
    <q-page-container>
      <q-page class="q-pa-none q-ma-none">
        <section class="relative-position full-height full-width overflow-hidden">
          <video autoplay muted loop playsinline class="video">
            <source src="src\media\main_page.mp4" type="video/mp4" />
          </video>
        </section>
      </q-page>
    </q-page-container>
  </q-layout>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const leftDrawerOpen = ref(false);

function toggleLeftDrawer() {
  leftDrawerOpen.value = !leftDrawerOpen.value;
}
</script>

<style scoped>
.video {
  object-fit: cover;
  z-index: -1;
}
</style>
