<template>
  <div class="container">
    <button @click="open = true" class="mybutton green">
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
import { ref } from 'vue'

const open = ref(false)
</script>

<style scoped>
.modal {
  position: fixed; /* or absolute, depending on your layout */
  z-index: 2; /* make sure the modal appears above the button */
  width: 100%;
  height: 100%;
}
</style>
