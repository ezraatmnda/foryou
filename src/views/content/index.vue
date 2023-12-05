<template>
  <Transition>
    <div v-if="show" class="modal-mask">
      <div class="modal-wrapper">
        <div class="modal-container">
          <h3>
            ERROR 404
          </h3>
          <hr class="divider"/>
          <button @click="$emit('close')" class="mybutton white">
            <span class="front white">
              Close
            </span>
          </button>
        </div>
      </div>
    </div>
  </Transition>
</template>

<script>
export default {
  name: 'Modal',
};
</script>

<script setup>
const props = defineProps({
  show: Boolean
})
</script>

<style>
.modal-mask {
  position: fixed;
  z-index: 9998;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: table;
  transition: opacity 0.3s ease;
}
.modal-wrapper {
  display: table-cell;
  vertical-align: middle;
}
.modal-container {
  font-family: press2p;
  width: 300px;
  margin: 0px auto;
  padding: 20px 30px;
  background-color: #731112;
  color: white;
  border-radius: 2px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.33);
  transition: all 0.3s ease;
  text-align: center;
}
.divider {
  color: white;
  margin-bottom: 20px;
}
</style>