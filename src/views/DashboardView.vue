<script setup></script>

<template>
  <main class="notes">
    <div>
      <h1 class="logo fs-1">this is the notes page</h1>
      <p>Notes is free note taking application...</p>
    </div>
  </main>
</template>

<style lang="scss" scoped>
.home {
  display: flex;
  flex-direction: column-reverse;
  justify-content: center;
  align-items: center;
  height: calc(100vh - 108px);
}
@media (min-width: 992px) {
  .home {
    display: flex;
    flex-direction: initial;
    justify-content: space-between;
    align-items: center;
  }
}
</style>
