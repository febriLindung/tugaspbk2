<template>
  <div class="content">
    <h2>{{ topic.title }}</h2>
    <p>{{ topic.content }}</p>
  </div>
</template>

<script>
export default {
  props: ['topic']
}
</script>

<style scoped>
.content {
  flex: 1;
  padding: 1rem;
}
</style>
