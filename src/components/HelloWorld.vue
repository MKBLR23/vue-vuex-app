<template>
  <div>
    <h1>{{ msg }}</h1>
    <p>Counter value is: {{ counter }}</p>
    <p>Counter incremental value by (10) is: {{ increment }}</p>
  </div>
</template>

<script>
import { mapGetters } from "vuex";

export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  computed: {
    ...mapGetters({
      counter: "addCurrencyToCounter",
      increment: "incrementCounterByTen"
    })
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
p {
  font-size: 40px;
}
</style>
