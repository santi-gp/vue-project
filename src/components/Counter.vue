<template>
  <div class="styleCounter">
    <div>
      <h4>Contador</h4>
      <div class="styleButton">
        <button @click="decrement">-</button>
        <strong> {{ count }} </strong>
        <button @click="increment">+</button>
      </div>
      <button class="reset" @click="reset" >Reset</button>
    </div>
  </div>
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
    reset(){
      this.count=0;
    }
  },
};
</script>
<style>
.styleCounter {
  width: 50%;
  margin: 0 auto;
  padding: 2%;
  background-color: #00c7f1;
  border-radius: 5px;
}
.styleCounter > div {
  display: grid;
  grid-template: 1fr;
  grid-gap: 1em;
}
.styleButton {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
button {
  background-color: #1d213a;
  color: #fff;
  border: none;
  padding: .5rem;
}
.reset{
  width: fit-content;
  
  margin: 0 auto;
}
</style>
