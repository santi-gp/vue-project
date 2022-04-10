<template>
  <header>
    <div className="logo">
      <h2>Logo</h2>
    </div>
    <Burger />
  </header>
</template>
<script>
import Burger from "./Burger.vue";
export default {
  name: "HeaderView",
  components: { Burger }
};
</script>