<template>
  <section class="boxCard">
    <div class="card">
      <p class="style-for-card"></p>
      <p>
        {{ $props.title }}
      </p>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'CardTask',
  props: {
    title: String
  },
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .boxCard {
    padding-top: 1rem;
    width: 100%;
  }
  .card {
    background-color: cyan;
    padding: 1rem;
    width: 100%;
  }
</style>
