<template>
  <header>
    <div class="margin-wrap">
      <div class="logo">
        <h2>Logo</h2>
      </div>
      <Burger />
    </div>
  </header>
</template>
<script>
import Burger from "./Burger.vue";
export default {
  name: "HeaderView",
  components: { Burger },
};
</script>