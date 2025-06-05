<template>
  <div class="container">
    <Sidebar :topics="topics" @topicSelected="selectedTopic = $event" />
    <Content :topic="topics[selectedTopic]" />
  </div>
</template>

<script>
import Sidebar from './components/Sidebar.vue'
import Content from './components/Content.vue'

export default {
  components: { Sidebar, Content },
  data() {
    return {
      selectedTopic: 0,
      topics: [
        { title: "Home", content: "Selamat datang di materi Pertemuan 2 dan 3." },
        { title: "Declarative Rendering", content: "Fitur inti vue adalah rendering deklatif: menggunkan sintaks templet yang memperluas HTML, kita dapat mendeskripsikan tampilan HTML berdasarkan status javascript." },
        { title: "Attribute Bindings", content: "Direktif adalah atribut khusus yang dimulai dengan awalan v-. mereka aadalah bagian dari sintaks template Vue." },
        { title: "Form Bindings", content: "Binding dalam Vue.js mengacu pada cara data terkait ke eleman HTML dalam tampllate Vue." },
        { title: "Conditional Rendering", content: "Binding dalam Vue.js mengacu pada cara data terkait ke eleman HTML dalam tampllate Vue." },
        { title: "List Rendering", content: "List rendering adalah salah satu sintaks unum yanng digunkan dalam pemngembangan veb front-end." },
        { title: "Computed Property", content: "Adalah opsi konfugurasi ketiga dalam intance Vue yang akan dipelajari." },
        { title: "Lifecycle dan Template Refs", content: "Setiap kali coponen mencapai tahap baru dalam siklus hidupnya,fungsi tertentu akan berjalan dan kita dapt menambahkan kode ke fungsi tersebut." },
        { title: "Watchers", content: "Memungkinkan kita untuk memantau sebagian data,atau properti yang dihitung" }
      ]
    };
  }
}
</script>

<style scoped>
.container {
  display: flex;
  height: 100vh;
}
</style>
