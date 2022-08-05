<template>
  <section>
    <article>
      <Fetch />
      <Vfor />
    </article>
  </section>
  <aside>
    <Counter />
    <Calculator title="Calculadora" />
    <Factorial />
  </aside>
</template>

<script>
import Counter from "@/components/Counter.vue";
import Vfor from "@/components/Vfor.vue";
import Calculator from "@/components/Calculator.vue";
import Factorial from "@/components/Factorial.vue";
import Fetch from "@/components/Fetch.vue";
// @ is an alias to /src

export default {
  components: { Counter, Vfor, Calculator, Factorial, Fetch },
  name: "HomeView",
};
</script>
