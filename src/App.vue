<script setup lang="ts">
import { RouterView } from "vue-router";
import NavBar from "@/components/NavBar.vue";
</script>

<template>
  <header>
    <div class="min-h-screen w-screen flex flex-col items-center">
      <NavBar />
      <div class="h-full w-full flex justify-center items-center max-w-7xl p-4">
        <RouterView v-slot="{ Component, route }">
          <component :is="Component" :key="route.path" />
        </RouterView>
      </div>
    </div>
  </header>
</template>
