<script setup>
  import { computed, ref } from 'vue';

  const active = ref(false);
  const activeString = computed(() => `${active.value}`);

  function toggleActive() {
    active.value = active.value === 'true' ? 'false' : 'true';
  }
</script>

<template>
  <main>
    <edje-spinner :active="activeString"></edje-spinner>
    <div style="position: fixed; top: 1em; left: 1em; z-index: 200000;">
      <button @click="toggleActive">Toggle</button>
    </div>
  </main>
</template>
