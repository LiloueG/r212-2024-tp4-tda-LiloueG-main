<script setup lang="ts">
import Card from '@/components/Card.vue'
</script>
<template>
  <div class="bg-[rgb(238_242_255)]">
    <div class="container py-20 space-y-8">
      <h1>Properties to rent</h1>
      <div class="grid md:grid-cols-2 xl:grid-cols-3 gap-8">
        <Card v-for="house in 6" :key="house" />
      </div>
    </div>
  </div>
</template>
