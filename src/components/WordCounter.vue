<template>
  <div class="counter">
    <textarea class="item textarea" v-model="text" />
    <div class="item result">
      <div>{{wordCount}} words</div>
      <div>{{characterCount}} characters</div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'WordCounter',
  data() {
    return {
      text: ''
    };
  },
  computed: {
    characterCount(): number {
      return this.text.length;
    },
    wordCount(): number {
      const text = this.text.trim();
      return text.length ? text.split(/[\s\r\n]+/).length : 0;
    }
  }
});
</script>

<style scoped>
.counter {
  display: flex;
  flex-direction: column;
  margin: auto;
  width: 30rem;
  align-items: center;
}
.item:not(:first-child) {
  margin-top: 8px;
}
.textarea {
  width: 100%;
  min-height: 3rem;
}
.result {
  align-self: flex-end;
  text-align: end;
}
</style>
