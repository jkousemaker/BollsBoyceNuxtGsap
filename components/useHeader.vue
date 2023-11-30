<script lang="js" setup>
const { $gsap: gsap } = useNuxtApp();
const asideToggled = ref(false);

function toggleAside() {
  asideToggled.value = !asideToggled.value;
  var tl = gsap.timeline({});
  if(asideToggled.value) {
    tl.to("#asideWrapper", {xPercent: 0, duration: 1});
  } else {
    tl.to("#asideWrapper", {xPercent: -100, duration: 1});
  }
}
</script>

<template>
  <div>
    <header>
      <h1 @click="toggleAside()">Menu</h1>
      <h2>BB</h2>
    </header>
    <useAside :state="asideToggled"></useAside>>
  </div>
</template>
