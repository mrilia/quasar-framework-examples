<template>
  <q-page padding>
    <input v-model="text" @keyup="calculateLen()" />
    <p class="text-grey2">Letter count: {{ textLen }}</p>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      text: "",
      textLen: 0,
    };
  },
  methods: {
    calculateLen() {
      this.textLen = this.text.length;
    },
  },
});
</script>
