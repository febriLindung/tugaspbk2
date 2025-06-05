<template>
  <div class="sidebar">
    <h3>Pertemuan 2 dan 3</h3>
    <ul>
      <li v-for="(topic, index) in topics" :key="index" @click="$emit('topicSelected', index)">
        {{ topic.title }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: ['topics']
}
</script>

<style scoped>
.sidebar {
  width: 250px;
  border-right: 1px solid #ccc;
  padding: 1rem;
}
li {
  list-style: none;
  margin: 10px 0;
  cursor: pointer;
}
li:hover {
  font-weight: bold;
}
</style>
