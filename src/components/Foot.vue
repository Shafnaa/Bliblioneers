<script setup>
import { ref } from "vue";
import ChevronDown from "./icons/ChevronDown.vue";
import ChevronUp from "./icons/ChevronUp.vue";

const collapse = ref(false);

function toggle() {
  collapse.value = !collapse.value;
}
</script>

<template>
  <footer>
    <p v-if="collapse" class="collapse">
      Lorem ipsum, dolor sit amet consectetur adipisicing elit. Enim deserunt
      fuga architecto dolore beatae consequatur natus optio earum tempora.
      Nostrum vero non quas eum qui aliquid nemo ex rerum voluptas! Lorem ipsum
      dolor sit amet consectetur adipisicing elit. Porro, quo atque illo maxime
      modi id, cum eveniet, quibusdam sit ipsa beatae? Minima, reprehenderit
      quos vel recusandae suscipit ipsam! Eligendi, iste?
    </p>
    <button v-if="collapse" @click="toggle" class="collapse-button">
      Collapse All <ChevronUp />
    </button>
    <button v-else @click="toggle" class="collapse-button">
      Show All <ChevronDown />
    </button>
    <p>©2022 PT Global Digital Niaga</p>
  </footer>
</template>

<style scoped>
footer {
  background-color: var(--color-whitesmoke);
  padding: 2em;
  text-align: center;
}

.collapse {
  text-align: left;
}

.collapse-button {
  background-color: transparent;
  border: none;
  color: var(--color-blue);
  font-weight: 500;
  margin-bottom: 8em;
}
</style>
