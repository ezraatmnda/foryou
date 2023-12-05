<template>
  <div class="container">
    <button @click="openModalWithDelay" class="mybutton green">
      <span class="front green">
        CLICK ME
      </span>
    </button>

    <Teleport to="body">
      <Modal :show="open" @close="open = false" />
    </Teleport>
  </div>
</template>

<script setup>
import Modal from './views/content/index.vue';
</script>

<script>
export default {
  data() {
    return {
      open: false,
    };
  },
  methods: {
    openModalWithDelay() {
      // Add a delay of 1000 milliseconds (1 second) before opening the modal
      setTimeout(() => {
        this.open = true;
      }, 500);
    },
  },
};
</script>

<style scoped>
</style>
