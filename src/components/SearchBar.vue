<script setup lang="ts">
import ArrowIcon from './icons/ArrowIcon.vue'
import { ref } from 'vue'
const address = ref('')
const search = () => {
  console.log(address.value)
}
</script>

<template>
  <div class="searchbar">
    <label for="address">
      <input
        v-on:keyup.enter="search"
        name="address"
        type="text"
        placeholder="Search for any IP address or domain"
        v-model.lazy="address"
      />
    </label>
    <button @click="search">
      <ArrowIcon />
    </button>
  </div>
</template>

<style scoped lang="scss">
.searchbar {
  width: 90%;
  height: 50px;
  background-color: white;
  border-radius: 10px;
  display: flex;
  align-items: center;
  padding: 0 20px;
  margin-top: 50px;
  margin-inline: auto;
  position: relative;
  @media screen and (min-width: 600px) {
    width: 500px;
  }
  label {
    width: 100%;
    height: 100%;
  }
  input {
    border: none;
    outline: none;
    width: 100%;
    height: 100%;
    font-size: 18px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }
  button {
    position: absolute;
    right: 0;
    background-color: #000;
    border: none;
    outline: none;
    width: 50px;
    height: 100%;
    border-radius: 0px 10px 10px 0px;
    margin-left: 20px;
    cursor: pointer;
    align-self: flex-end;
  }
}
</style>
