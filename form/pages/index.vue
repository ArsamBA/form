<template>
  <div class="container">
    <Landing :title="title" :description="description" :buttonText="buttonText">
      // import landing svg
    </Landing>
  </div>
  <div style="border-top: 1px solid #a0a0a0; display: block; width: 100% ;"></div>
  <div class="container">
    // import main component
  </div>
</template>

<script setup lang="ts">
const title = ref("")
const description = ref("")
const buttonText = ref("")
</script>

<style lang="scss">
@import '@/assets/scss/global.scss';

</style>