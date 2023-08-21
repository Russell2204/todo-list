<template>
  <Navbar @searchValue="search = $event" />
  <Modal @showOrHideModal="showOrHideModal" v-show="showModal" />
  <a href="#" class="addNote" @click.prevent="showModal = true">
    <img src="@/assets/img/edit.svg" alt="">
  </a>
  
</template>
<script>
import Modal from './components/Modal.vue'
import Navbar from './components/Navbar.vue'
  export default {
    data() {
      return {
        showModal: false,
      }
    },
    methods: {
      showOrHideModal(){
        this.showModal = false
      },
    },
    
    components: { Navbar, Modal },
}
</script>
<style>

</style>