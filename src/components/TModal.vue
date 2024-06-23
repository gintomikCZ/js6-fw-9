<script>
export default {
  data() {
    return {
      open: false
    }
  },
  methods: {
    onClick () {
      this.$emit('clicked')
      this.open = false
    }
  },
  emits: [ 'clicked' ]
}
</script>

<template>
  <button @click="open = true">Open Modal</button>

  <Teleport to=".teleport-area">
    <div v-if="open" class="modal">
      <p>Hello from the modal!</p>
      <button @click="onClick">Close</button>
    </div>
  </Teleport>
</template>

<style scoped>
.modal {
  position: fixed;
  z-index: 999;
  top: 20%;
  left: 50%;
  width: 300px;
  margin-left: -150px;
}
</style>