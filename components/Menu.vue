<template>
  <nav class="">
    <ul class="flex flex-row gap-2">
      <MenuListItem href="/" text="Home" :active="Boolean(route.name === 'index')" />
      <MenuListItem href="/about" text="About" :active="Boolean(route.name === 'about')" />
      <MenuListItem href="/shop" text="Shop" :active="Boolean(route.name === 'shop')" />
      <MenuListItem href="/contact" text="Contact" :active="Boolean(route.name === 'contact')" />
    </ul>
  </nav>
</template>

<script setup lang="ts">
const route = useRoute();

</script>

<style>

</style>