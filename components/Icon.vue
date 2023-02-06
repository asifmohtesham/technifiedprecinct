<template>
  <div :class="`w-32 h-32 ${classList}`" v-if="icon" v-html="icon"></div>
</template>

<script setup lang="ts">
const props = defineProps<{
  name: string,
  classList?: string,
}>();

// Auto-load icons
const icons = Object.fromEntries(
  Object.entries(import.meta.glob('~/images/*.svg', { as: 'raw' })).map(
    ([key, value]) => {
      const filename = key.split('/').pop()!.split('.').shift()
      return [filename, value]
    },
  ),
)

// Lazily load the icon
const icon = props.name && (await icons?.[props.name]?.())
</script>

<style>

</style>