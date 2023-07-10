<template>
  <form class="section-group">
    <input 
      type="text"
      class="input-text"
      id="title" 
      placeholder="EX: fazer relatório"
      v-model="title">
    <button 
      type="button"
      @click="createTask"
      class="button-create"
    >
      Criar tarefa
    </button>
  </form>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

  export default defineComponent({
    name: "FormTask",
    emits: ["saveTask"],
    data() {
      return {
        title: ''
      }
    },
    methods: {
      createTask() {
        this.$emit("saveTask", this.title)
        this.title = ""
      }
    }
  })
</script>

<style scoped>
  .input-text {
    padding: .5rem;
    border-radius: .3rem;
    font-size: .9rem;
    width: 20rem;
  }
  .button-create {
    padding: .7rem;
    border-radius: .3rem;
    font-size: .9rem;
    border: none;
    background-color: cyan;
    cursor: pointer;
  }
  .button-create:hover {
    opacity: 0.86;
  }
  .section-group {
    display: flex;
    flex-direction: row;
    gap: 1rem;
  }
</style>