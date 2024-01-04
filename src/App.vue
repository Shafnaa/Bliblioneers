<script setup>
import Foot from "./components/Foot.vue";
import Navbar from "./components/Navbar.vue";
import FirstLayout from "./components/FirstLayout.vue";
import SecondLayout from "./components/SecondLayout.vue";
import ThirdLayout from "./components/ThirdLayout.vue";
import FourthLayout from "./components/FourthLayout.vue";
import ProductContainer from "./components/ProductContainer.vue";

const target = document.getElementById("app");

function handleClick() {
  target.scrollTo({
    top: 0,
    behavior: "smooth",
  });
}
</script>

<template>
  <header id="#home">
    <Navbar />
  </header>

  <main>
    <FirstLayout />
    <SecondLayout />
    <ProductContainer />
    <ThirdLayout />
    <FourthLayout />
  </main>

  <button @click="handleClick">
    <svg
      height="24"
      width="24"
      clip-rule="evenodd"
      fill-rule="evenodd"
      stroke-linejoin="round"
      stroke-miterlimit="2"
      viewBox="0 0 24 24"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="m9.001 10.978h-3.251c-.412 0-.75-.335-.75-.752 0-.188.071-.375.206-.518 1.685-1.775 4.692-4.945 6.069-6.396.189-.2.452-.312.725-.312.274 0 .536.112.725.312 1.377 1.451 4.385 4.621 6.068 6.396.136.143.207.33.207.518 0 .417-.337.752-.75.752h-3.251v9.02c0 .531-.47 1.002-1 1.002h-3.998c-.53 0-1-.471-1-1.002z"
        fill-rule="nonzero"
        fill="currentColor"
      />
    </svg>
  </button>

  <Foot />
</template>

<style scoped>
main {
  gap: 2em;
}

a,
button {
  width: 3em;
  height: 3em;
  position: fixed;
  display: flex;
  justify-content: center;
  align-items: center;
  color: var(--color-blue);
  background-color: var(--color-white);
  border: none;
  border-radius: 100%;
  bottom: 4em;
  right: 4em;
}
</style>
