<template>
  <nav>
    <img src="../assets/logo.svg" alt="blibli" />
  </nav>
</template>

<style scoped>
nav {
  background-color: var(--color-blue);
  display: flex;
  padding: 1.5em;
  justify-content: center;
  align-items: center;
}

@media (min-width: 801px) {
  nav {
    justify-content: flex-start;
    padding-left: 4em;
  }
}
</style>
