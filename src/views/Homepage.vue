<script setup lang="ts">
import InfoBox from '@/components/InfoBox.vue'
import SearchBar from '@/components/SearchBar.vue'
</script>

<template>
  <header class="header">
    <div class="header__background">
      <h1 class="header__title">IP Address Tracker</h1>
      <SearchBar />
    </div>
  </header>

  <main class="box__wrapper">
    <InfoBox title="Ip address" />
    <InfoBox title="Location" />
    <InfoBox title="timezone" />
    <InfoBox title="isp" />
  </main>
</template>

<style scoped lang="scss">
.header {
  width: 100%;

  &__background {
    padding: 0 20px;
    background-image: url(/public/images/pattern-bg-desktop.png);
    width: 100%;
    height: 300px;
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
  }
  &__title {
    text-align: center;
    color: white;
    font-size: 44px;
    line-height: 48px;
    padding-top: 20px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }
}
</style>
