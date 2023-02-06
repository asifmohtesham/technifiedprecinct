<template>
  <a :href="href" class="card p-2 text-2xl text-center text-yellow-800 hover:text-yellow-100 hover:bg-yellow-800 border border-double border-yellow-800 hover:border-yellow-100 rounded fill-yellow-800 hover:fill-yellow-100 transition">
    <Icon v-if="img" :name="img" />

    <span class="">
      {{ text }}
    </span>
  </a>
</template>

<script lang="ts">
export default {
 props: {
  href: String,
  text: String,
  img: String,
 }
}

</script>

<style>

</style>