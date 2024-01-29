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
    <InfoBox custom-style="box" title="Ip address" content="192.212.174.101" />
    <InfoBox custom-style="box" title="Location" content="Brooklyn, NY 10001" />
    <InfoBox custom-style="box" title="timezone" content="UTC - 05:00" />
    <InfoBox custom-style="box" title="isp" content="SpaceX Starlink" />
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

.box__wrapper {
  display: flex;
  justify-content: space-between;
  flex-direction: column;
  width: 80%;

  background-color: white;
  border-radius: 10px;
  box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.75);
  margin-inline: auto;
  margin-top: -100px;
  z-index: 1;
  padding: 20px;
  @media screen and (min-width: 768px) {
    flex-direction: row;
    height: 200px;
  }
  .box {
    width: 100%;
    padding: 0 20px;
    margin-top: 20px;
    @media screen and (min-width: 768px) {
      width: 25%;
      margin-top: 0;
    }
  }
  .box:not(:last-child) {
    border-bottom: 1px solid #ccc;
    padding-bottom: 20px;
    @media screen and (min-width: 768px) {
      border-bottom: none;
      border-right: 1px solid #ccc;
    }
  }
}
</style>
