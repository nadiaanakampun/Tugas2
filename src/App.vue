<template>
  <div>
    <!-- Binding dengan class dan style -->
    <input type="text" class="text-input" :class="{ 'highlight': isHighlighted }" :style="{ 'font-weight': isBold ? 'bold' : 'normal' }" v-model="inputText">

    <!-- Interaksi dinamis dengan event listeners -->
    <button @click="toggleHighlight">Toggle Highlight</button>
    <button @click="toggleBold">Toggle Bold</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputText: '',
      isHighlighted: false,
      isBold: false
    };
  },
  methods: {
    toggleHighlight() {
      this.isHighlighted = !this.isHighlighted;
    },
    toggleBold() {
      this.isBold = !this.isBold;
    }
  }
};
</script>

<style scoped>
.text-input {
  width: 200px;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
  margin-bottom: 10px;
}
.highlight {
  background-color: yellow;
}
</style>
