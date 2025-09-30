<template>
  <div class="contenedor">
    <form class="formulario">
      <div>
        <label for="nombre">Nombre:</label>
        <input type="text" id="nombre" v-model="nombre" required />
      </div>

      <div>
        <label for="email">Email:</label>
        <input type="email" id="email" v-model="email" required />
      </div>

      <div>
        <label for="telefono">Teléfono:</label>
        <input type="tel" id="telefono" v-model="telefono" />
      </div>

      <button type="button">Enviar</button>
    </form>

    <div class="datos">
      <h3>Datos ingresados:</h3>
      <p><strong>Nombre:</strong> {{ nombre }}</p>
      <p><strong>Email:</strong> {{ email }}</p>
      <p><strong>Teléfono:</strong> {{ telefono }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nombre: "",
      email: "",
      telefono: "",
    };
  },
};
</script>

<style scoped>
.contenedor {
  display: flex;
  justify-content: center;
  align-items: flex-start;
  gap: 50px;
  padding: 50px;
}

.formulario {
  display: flex;
  flex-direction: column;
  width: 300px;
}

.formulario div {
  margin-bottom: 10px;
}

input {
  width: 100%;
  padding: 5px;
  box-sizing: border-box;
  background-color: cadetblue;
}

button {
  padding: 8px;
  background-color: #30b171;
  border: 1px solid #ccc;
  cursor: pointer;
}

.datos {
  max-width: 300px;
}
</style>
