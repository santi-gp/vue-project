<template>
  <strong> Contador: {{ count }} </strong>
  <button @click="increment">+</button>
  <button @click="decrement">-</button>
</template>
<script>
export default {
  name: "Counter",
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    increment() {
      this.count++;
    },
    decrement() {
      this.count--;
    },
  },
};
</script>