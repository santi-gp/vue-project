<template>
  <section>
    <h2>Inicio</h2>
    <article>
      <Vfor />
    </article>
  </section>
  <aside>
    <Counter />
  </aside>
</template>

<script>
import Counter from "@/components/Counter.vue";
import Vfor from "@/components/Vfor.vue";
// @ is an alias to /src

export default {
  components: { Counter, Vfor },
  name: "HomeView",
};
</script>
