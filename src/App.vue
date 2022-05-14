<template>
 <h1>{{ title }}</h1>
 <teleport to=".modals" v-if="showModal">
     <Modal theme="sale" @close="toggleModal">
        <template v-slot:links>
          <a href="#">Sign up now!</a>
          <a href="#">More Info</a>
        </template>
        <h1>Ninja Givaway</h1>
        <p>Grab your ninja swag for half price!</p>
    </Modal>
 </teleport>

 <teleport to=".modals" v-if="showModalTwo">
     <Modal theme="sale" @close="toggleModalTwo">
        <h1>Sign Up to the Newsletter</h1>
        <p>For Updates and Promo Codes</p>
    </Modal>
  </teleport>
 <button @click.alt="toggleModal">Open (alt)</button>
 <button @click="toggleModalTwo">Open</button>
</template>

<script>
import ModalVue from "./components/Modal.vue"
import Modal from "./components/Modal.vue"

export default {
  name: 'App',
  components: { ModalVue, Modal },
  data() {
    return {
      title: '¡Hola, Pendejo!',
      showModal: false,
      showModalTwo: false
    }
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal
    },
    toggleModalTwo() {
      this.showModalTwo = !this.showModalTwo
    }
  }
}

</script> 

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center; 
  color: #2c3e50;
  margin-top: 60px;
}


</style>
