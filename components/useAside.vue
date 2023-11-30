<script lang="ts" setup>
const props = defineProps({
  state: Boolean,
});
</script>

<template>
  <div
    class="absolute w-full h-full top-0 left-0 pointer-events-none"
    id="asideWrapper"
  >
    <aside class="h-full w-1/3 bg-black/50">
      <h2>Close</h2>
    </aside>
  </div>
</template>
