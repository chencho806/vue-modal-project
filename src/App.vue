<template>
 <h1>{{ title }}</h1>
 <ModalVue 
    header="Sign Up For Mailing List" 
    text="Be on the look out for our giveaways!"/>
</template>

<script>
import ModalVue from "./components/Modal.vue"

export default {
  name: 'App',
  components: { ModalVue },
  data() {
    return {
      title: '¡Hola, Pendejo!'
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
