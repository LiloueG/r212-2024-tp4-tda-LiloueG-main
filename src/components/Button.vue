<script setup lang="ts">

const props = defineProps<{
  variant?:  'default' | 'outline'
  size?: 'sm' | 'md' | 'lg'
  url?: string
  text?: string
  icon?: string | object | undefined
}>()

{variant: 'default'}
{size: 'sm'}

const variantClass = {
  default: 'bg-indigo-500 text-white',
  outline: 'bg-transparent border border-indigo-200 text-indigo-500',
}

const sizeClass = {
  sm: 'py-1 px-2 text-sm',
  md: 'py-2 px-4 text-base',
  lg: 'py-3 px-6 text-lg',
}

</script>
<template> 
    <RouterLink :to="`${url}`" class="inline-flex items-center gap-1 font-bold" :class="[sizeClass[props.size], variantClass[props.variant]]">
        <component class="w-5 h-5" :is="props.icon"></component>
        {{  text }}
    </RouterLink>
</template>