<template>
  <form @submit.prevent="onSubmit">
    <div>
      <label>Nombre</label>
      <input type="text" v-model="form.firstName" />
    </div>
    <div>
      <label>Apellidos</label>
      <input type="text" v-model="form.lastName" />
    </div>
    <div>
      <label>Correo</label>
      <input type="text" v-model="form.email" />
    </div>
    <div>
      <button type="submit">Enviar</button>
    </div>
  </form>
</template>
<script>
export default {
  name: "FormSimple",
  data() {
    return {
      form: {
        firstName: "",
        lastName: "",
        email: "",
      },
    };
  },
  methods: {
    onSubmit() {
      /*console.log("click");*/
      if (!this.formValidate) return;
      console.log("Enviar Formulario");
    },
  },
  computed: {
    formValidate() {
      return (
        this.form.firstName.length > 0 &&
        this.form.lastName.length > 0 &&
        this.form.email.length > 0
      );
    },
  },
};
</script>
<style scoped>
form {
  margin: 0 auto;
  width: 50%;
  display: flex;
  flex-direction: column;
}
form div {
  display: flex;
  flex-direction: column;
  margin: 1% 0;
}
button {
  width: max-content;
  padding: 1.25% 1.5%;
}
</style>>

