<template>
  <q-page>
    <div class="box fixed-center text-center">
      <div>
        <h3>{{ counter }}</h3>
        <q-btn
          @click="decreaseCounter()"
          outline
          round
          color="primary"
          icon="remove"
          size="sm"
        />
        <q-btn
          @click="increaseCounter()"
          outline
          round
          color="primary"
          icon="add"
          size="sm"
        />
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      counter: 0,
    };
  },
  methods: {
    increaseCounter() {
      this.counter++;
    },
    decreaseCounter() {
      this.counter--;
    },
  },
});
</script>
<style scoped>
.box {
  width: 200px;
  height: 250px;
  border: 2px solid grey;
}
</style>
