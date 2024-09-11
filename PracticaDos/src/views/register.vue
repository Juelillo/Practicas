<!-- src/views/Register.vue -->
<template>
    <div class="container mt-5">
      <h2>Registrar</h2>
      <form @submit.prevent="submitRegister">
        <div class="mb-3">
          <label for="name" class="form-label">Nombre</label>
          <input type="text" v-model="name" class="form-control" id="name" required>
        </div>
        <div class="mb-3">
          <label for="email" class="form-label">Correo Electrónico</label>
          <input type="email" v-model="email" class="form-control" id="email" required>
        </div>
        <div class="mb-3">
          <label for="password" class="form-label">Contraseña</label>
          <input type="password" v-model="password" class="form-control" id="password" required>
        </div>
        <button type="submit" class="btn btn-primary">Registrar</button>
      </form>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        name: '',
        email: '',
        password: ''
      }
    },
    methods: {
      submitRegister() {
        // Aquí puedes agregar tu lógica de registro
        alert(`Registrando usuario con: ${this.email}`);
      }
    }
  }
  </script>
  