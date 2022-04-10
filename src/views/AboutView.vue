<template>
  <section>
    <h2>About</h2>
    <article>
      <router-view />
    </article>
  </section>
  <aside>
    <Accordion title="Accordion">
      <router-link to="/about/aboutInfo">About Info</router-link>
    </Accordion>
  </aside>
</template>
<script>
import Accordion from "@/components/Accordion.vue";
export default {
  name: "AboutView",
  components: { Accordion },
};
</script>