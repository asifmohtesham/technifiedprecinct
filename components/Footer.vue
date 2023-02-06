<template>
  <footer class="fixed inset-0 bottom-0 top-auto p-4 bg-slate-800 text-yellow-50 flex flex-row">
    <h6>&copy; {{ year }}</h6>
    &nbsp;
    &VerticalLine;
    &nbsp;
    <span class="font-bold">
      Technified Precinct LLC
    </span>
  </footer>
</template>

<script lang="ts">
export default {
  data: function () {
    return {
      year: new Date().getFullYear()
    }
  }

}
</script>

<style>

</style>