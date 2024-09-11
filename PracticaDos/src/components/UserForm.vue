<template>
  <div class="mb-4 fondoTabla p-4 rounded">
    <h2>Registrar Usuario</h2>
    <form @submit.prevent="submitForm">
      <div class="mb-3 texto">
        <label for="name" class="form-label">Nombre</label>
        <input type="text" class="form-control" v-model="user.name" id="name" required />
      </div>
      <div class="mb-3 texto">
        <label for="email" class="form-label">Correo Electrónico</label>
        <input type="email" class="form-control" v-model="user.email" id="email" required />
      </div>
      <div class="mb-3 texto">
        <label for="age" class="form-label">Edad</label>
        <input type="number" class="form-control" v-model="user.age" id="age" required />
      </div>
      <button type="submit" class="btn btn-primary">Registrar</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      user: {
        name: '',
        email: '',
        age: ''
      }
    };
  },
  methods: {
    submitForm() {
      // Emitir el evento al componente padre con los datos del usuario
      this.$emit('user-registered', { ...this.user });
      // Limpiar el formulario
      this.user.name = '';
      this.user.email = '';
      this.user.age = '';
    }
  }
};
</script>

<style scoped>
.fondoTabla {
  background-color: #939596;
}
.texto{
  font:bold;
  font-size: medium;
}
</style>
