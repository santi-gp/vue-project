<template>
  <div class="accordion">
    <div class="headerAccordion" @click="isOpen = !isOpen">
      {{ title }}
    </div>
    <div class="contenAccordion" :class="isOpen ? 'open' : 'close'">
      <slot />
    </div>
  </div>
</template>

<script>
export default {
  name: "Accordion",
  props: {
    title: String,
    /*content: String,*/
  },
  data() {
    return {
      isOpen: false,
    };
  },
};
</script>
<style scoped>
.accordion {
  display: flex;
  flex-direction: column;
  width: 80%;
}
.headerAccordion {
  background-color: #0edddd;
  cursor: pointer;
}
.open {
  display: block;
  background-color: #acddf0;
}
.close {
  display: none;
}
</style>