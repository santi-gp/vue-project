<template>
  <section>
    <h1>hola</h1>
    <article>
      <router-view />
    </article>
  </section>
  <aside>
    <Accordion title="Formularios">
      <router-link to="/about/aboutInfo">Formulario Simple</router-link>
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