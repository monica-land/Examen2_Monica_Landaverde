<template>
  <div>
    <form @submit.prevent="handleSubmit">
      <div>
        <label for="nombre">Nombre:</label>
        <input type="text" id="nombre" v-model="nombre" required />
      </div>

      <div>
        <label for="email">Email:</label>
        <input type="email" id="email" v-model="email" required />
      </div>

      <button type="submit">Enviar</button>
    </form>

    <div v-if="enviado">
      <p>Formulario enviado correctamente:</p>
      <p><strong>Nombre:</strong> {{ nombre }}</p>
      <p><strong>Email:</strong> {{ email }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nombre: "",
      email: "",
      enviado: false,
    };
  },
  methods: {
    handleSubmit() {
      this.enviado = true;
      console.log("Formulario enviado:", this.nombre, this.email);
    },
  },
};
</script>

<style scoped>
form {
  margin: 20px;
}
input {
  margin-bottom: 10px;
}
</style>
