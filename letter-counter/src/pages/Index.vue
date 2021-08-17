<template>
  <q-page padding>
    <div class="fixed-center">
      <q-input outlined label="Type here" v-model="text" @keyup="calculateLen()" />
      <p class="text-grey">Letter count: {{ textLen }}</p>
    </div>
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
