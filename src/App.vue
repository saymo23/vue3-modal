<script>
import { ref } from 'vue'
import Modal from './components/Modal.vue'

export default {
  components: {
    Modal
  },
  setup(){
    const isOpen = ref(false)

    const openModal = () => {
      isOpen.value = true
      //HERE OTHER CHANGES

      return isOpen.value
    }

    return{
      isOpen, openModal
    }
  }
}

</script>

<template>
  <button @click="openModal">
    Open Modal
  </button>
  <Modal :open="isOpen" @close="isOpen = !isOpen" />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
