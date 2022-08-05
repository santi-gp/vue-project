<template>
  <form>
    <fieldset>
      <h3 class="txt-center my-1">
        {{ title }}
      </h3>
    </fieldset>
    <fieldset class="flex-row jc-center">
      <input size="6" type="text" v-model="sum1" />+
      <input size="6" type="text" v-model="sum2" />={{ sum }}
    </fieldset>
    <fieldset class="flex-row jc-center">
      <input size="6" type="text" v-model="sub1" />-
      <input size="6" type="text" v-model="sub2" />={{ sub }}
    </fieldset>
  </form>
</template>
<script>
export default {
  name: "Calculator",
  props: {
    title: String,
  },
  data() {
    return {
      sum1: "0",
      sum2: "0",
      sub1: "0",
      sub2: "0",
    };
  },
  computed: {
    sum: function () {
      let sum1 = parseFloat(this.sum1 === "" ? "0" : this.sum1);
      let sum2 = parseFloat(this.sum2 === "" ? "0" : this.sum2);
      return sum1 + sum2;
    },
    sub: function () {
      let sub1 = parseInt(this.sub1 === "" ? "0" : this.sub1);
      let sub2 = parseInt(this.sub2 === "" ? "0" : this.sub2);
      return sub1 + sub2;
    },
  },
};
</script>
