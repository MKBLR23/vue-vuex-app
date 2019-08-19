<template>
  <div>
    <md-button class="md-raised md-primary" @click="increase"
      >Increase</md-button
    >
    <md-button class="md-raised md-accent" @click="decrease"
      >Decrease</md-button
    >
    <md-button class="md-raised md-primary" @click="asyncIncrease(5)"
      >Async Increase by 5</md-button
    >
  </div>
</template>

<script>
import { mapActions } from "vuex";
export default {
  name: "app-counter",
  methods: {
    ...mapActions({
      increase: "increase",
      decrease: "decrease"
    }),
    asyncIncrease(incrementalValue) {
      const objectValue = {
        incrementalValue
      };
      this.$store.dispatch("asyncIncrement", objectValue);
    }
  }
};
</script>

<style>
button {
  margin: 10px;
  width: 170px;
  height: 60px;
  font-size: 40px;
}
</style>
