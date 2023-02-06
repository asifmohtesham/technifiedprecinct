<template>
  <li :id="String(route.name)">
    <NuxtLink v-if="target === false" :class="`${data.classList}`" :to="href">
      {{ text }}
    </NuxtLink>

    <a v-else :class="`${data.classList}`" :href="href" target="_blank" rel="noopener noreferrer">{{ text }}</a>
  </li>
</template>

<script setup lang="ts">
const route = useRoute();

const props = defineProps({
  href: String,
  text: String,
  target: Boolean,
  active: Boolean,
});

const data = {
  classList: "p-2 rounded border border-solid border-red-800 hover:bg-red-100 hover:text-red-900 transition",
}
if(props.active) {
  data.classList += ' text-red-900 bg-red-100';
} else {
  data.classList += ' text-red-100';
}
</script>

<style>

</style>