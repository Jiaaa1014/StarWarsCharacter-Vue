<template>
  <div id="app">
    <h2>{{title}}</h2>
    <h6 style="color:#666;">{{subtitle}}</h6>
    <div class="char-box">
      <Character
      v-for="(id, key) in init_ids"
      :id="id"
      :key="key"/>
    </div>
  </div>
</template>

<script>
import Character from "./components/Character.vue";

export default {
  name: "app",
  data() {
    return {
      title: "Who Do U Want to Keep in Your Team?",
      subtitle: "Click the box and randomly replaced with another guy ",
      init_ids: Array(5)
        .fill()
        .map(e => Math.floor(Math.random() * 87) + 1)
    };
  },
  components: {
    Character
  }
};
</script>
