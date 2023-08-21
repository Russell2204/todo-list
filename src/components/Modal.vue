<template>
<Transition name="modal">
  <div class="modal" @click="closeModal">
    <div class="modal-block" @click.stop>
      <div class="modal-content">
        <h2>Добавить заметку</h2>
        <input type="text" placeholder="Tile" v-model="title" />
        <textarea placeholder="Content" v-model="descr"></textarea>
        <div class="modal-btns">
          <a href="#" class="btn cancel" @click.prevent="closeModal">ОТМЕНА</a>
          <a href="#" class="btn">ДОБАВИТЬ</a>
        </div>
      </div>
    </div>
  </div>
</Transition >
</template>

<script>
export default {
  data() {
    return {
      title: "",
      descr: "",
    };
  },
  methods: {
    closeModal() {
        this.$emit("showOrHideModal")
        this.title = this.descr = ""
    },
  },
};
</script>

<style>
</style>