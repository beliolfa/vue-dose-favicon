<template>
  <div class="container">
    <div class="container">
      <nuxt-link to="geography">Geography</nuxt-link>
      <nuxt-link to="history">History</nuxt-link>
      <nuxt-link to="sports">Sports</nuxt-link>
    </div>
    <nuxt />
  </div>
</template>

<style>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  margin: 40px;
}
</style>
