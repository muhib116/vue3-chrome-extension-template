<template>
    <div class="grid grid-cols-2">
        <Input 
          type="number"
          min="0"
          max="1"
          step="0.1"
          title="Ex: between 0 and 1, like: 0.5"
          class="px-2 py-1 rounded"
          v-model="imageData.opacity"
          placeholder="Opacity"
          label="Opacity"
        />
        <Input 
          type="number"
          class="px-2 py-1 rounded"
          v-model="imageData.zIndex"
          placeholder="Z-Index"
          label="Z-Index"
        />
    </div>
</template>

<script setup>
    import { inject } from 'vue'
    import Input from '@/components/Input.vue'

    const { imageData } = inject('useConfig')
</script>