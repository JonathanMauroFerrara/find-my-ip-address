<script setup lang="ts">
import InfoBox from '@/components/InfoBox.vue'
import SearchBar from '@/components/SearchBar.vue'
</script>

<template>
  <header class="header">
    <div
      class="header__background"
      :style="{ 'background-image': 'url(/public/images/pattern-bg-desktop.png)' }"
    ></div>
    <h1 class="header__title">IP Address Tracker</h1>
    <SearchBar />
  </header>

  <main class="box__wrapper">
    <InfoBox title="Ip address" />
    <InfoBox title="Location" />
    <InfoBox title="timezone" />
    <InfoBox title="isp" />
  </main>
</template>

<style scoped>
.container {
}

.header {
  width: 100%;
}
.header__background {
  width: 100%;
  height: 300px;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
</style>
