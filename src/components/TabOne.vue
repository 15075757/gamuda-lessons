<template>
  <div>
    <h2>{{ tabName }}</h2>
    <p>Some content for {{ tabName }}</p>
    <v-text-field v-model="inputValue" label="Input"></v-text-field>
  </div>
</template>

<script>
export default {
  props: {
    tabName: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      inputValue: '',
    };
  },
  activated() {
    console.log(`${this.tabName} activated`);
  },
  deactivated() {
    console.log(`${this.tabName} deactivated`);
  },
};
</script>