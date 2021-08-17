<template>
  <q-page
    class="flex flex-center"
    v-bind:style="{'background-color':colors[colorIndex]}"
  >
    <q-btn
      @click="setNextColor()"
      rounded
      color="black"
      label="Click to change color"
    />
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      colorIndex: 0,
      colors: ["#B29DD9", "#FDFD98", "#FE6B64", "#77DD77", "#779ECB"],
    };
  },
  methods: {
    setNextColor() {
      this.colorIndex == this.colors.length - 1
        ? (this.colorIndex = 0)
        : this.colorIndex++;
    },
  },
});
</script>
