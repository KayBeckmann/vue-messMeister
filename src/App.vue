<template>
  <div class="center">
    <nav>
      <RouterLink to="/">Home</RouterLink> |
      <RouterLink to="/about">About</RouterLink>
    </nav>
    <RouterView />
  </div>
</template>

<style scoped>
.center {
  text-align: center;
}
</style>
