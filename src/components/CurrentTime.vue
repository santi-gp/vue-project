<template>
  <div class="cardBox">
    <div class="container">
      <h2>Hoy es:</h2>
      <h3>{{ getCurrentDate }}</h3>
    </div>
  </div>
</template>
<script>
export default {
  name: "CurrentTime",
  computed: {
    getCurrentDate() {
      const browserLocale =
        navigator.languages && navigator.languages.length
          ? navigator.languages[0]
          : navigator.language;
      const intlDateTime = new Intl.DateTimeFormat(browserLocale, {
        year: "numeric",
        month: "numeric",
        day: "numeric",
        hour: "numeric",
        minute: "numeric",
      });
      return intlDateTime.format(new Date());
    },
  },
};
</script>

<style>
.cardBox {
  box-shadow: 0 5px 10px 0 #50242433;
  transition: 0.3s linear;
  max-width: 33%;
  border-radius: 3px;
  margin: 20px;
}
.cardBox:hover {
  box-shadow: 0 10px 20px 0 #614f4f33;
}
.cardBox > .container {
  padding: 4px 18px;
}
</style>