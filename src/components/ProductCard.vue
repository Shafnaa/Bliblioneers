<script setup>
defineProps({
  price: {
    type: Number,
    required: true,
  },
  discount: {
    type: Number,
    required: false,
  },
  imgUrl: {
    type: String,
    required: false,
  },
  altText: {
    type: String,
    required: false,
  },
});
</script>

<template>
  <div class="card">
    <div v-if="imgUrl" class="card-image">
      <img src="../assets/R.webp" alt="product" />
    </div>
    <div v-else class="card-image">
      <img src="../assets/logo.svg" alt="blibli" />
    </div>
    <div class="card-detail">
      <h3 class="card-title">
        <slot name="title"></slot>
      </h3>
      <div v-if="discount" class="card-price">
        <i
          >Rp{{ ((price * (100 - discount)) / 100).toLocaleString("de-DE") }}</i
        >
        <div style="display: flex; gap: 4px; color: gray; align-items: center">
          <p style="text-decoration: line-through">
            Rp{{ price.toLocaleString("de-DE") }}
          </p>
          <span class="card-discount">{{ discount }}%</span>
        </div>
      </div>
      <div v-else>
        <i>Rp{{ price.toLocaleString("de-DE") }}</i>
      </div>
    </div>
    <button class="card-button">Add to bag</button>
  </div>
</template>

<style scoped>
.card {
  width: 132px;
  display: flex;
  flex-direction: column;
  border: 1px solid var(--color-whitesmoke);
  filter: drop-shadow(0 0 0.125em var(--color-gray));
  border-radius: 1em;
  overflow: hidden;
  color: var(--color-black);
  background-color: var(--color-white);
}

.card-image {
  width: 100%;
  aspect-ratio: 1;
  background-color: var(--color-whitesmoke);
}

img {
  width: 100%;
  height: 100%;
  object-fit: contain;
}
.card-detail {
  padding: 0.5em;
  background-color: var(--color-white);
}

.card-title {
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 2;
  overflow: hidden;
  font-weight: 600;
}

i {
  font-style: normal;
  font-weight: bold;
  color: var(--color-orange);
}

.card-discount {
  background-color: rgba(255, 0, 0, 0.2);
  color: var(--color-red);
  padding: 0.25em 0.5em;
  border-radius: 100cqmax;
}

.card-button {
  background-color: var(--color-blue);
  border: none;
  color: var(--color-white);
  padding: 0.5em;
  font-weight: bold;
  border-radius: 0.5em;
  margin: 0.5em;
  margin-top: auto;
}

@media (min-width: 801px) {
  .card {
    width: 182px;
  }

  .card-detail {
    gap: 0.25em;
  }
}
</style>
