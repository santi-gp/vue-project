<template>
<div>
<h3 class="my-1">Factorial</h3>
  <input size="6" type="text" v-model="num" />=<span> {{ result }}</span>
</div>

</template>
<script>
export default {
  name: "Factorial",
  data() {
    return {
      num: '0'
    };
  },
  methods: {
    factorial(x = this.num) {
      if (x === 0 || x === 1) {
        return 1;
      } else return x * this.factorial(x - 1);
    },
  },
  computed: {
    result: function () {
      let num = parseFloat(this.num === "" ? "0" : this.num);
      return this.factorial(num);
    },
  },
};
</script>
