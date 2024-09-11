<!-- src/views/Login.vue -->
<template>
    <div class="container mt-5">
      <h2>Iniciar Sesión</h2>
      <form @submit.prevent="submitLogin">
        <div class="mb-3">
          <label for="email" class="form-label">Correo Electrónico</label>
          <input type="email" v-model="email" class="form-control" id="email" required>
        </div>
        <div class="mb-3">
          <label for="password" class="form-label">Contraseña</label>
          <input type="password" v-model="password" class="form-control" id="password" required>
        </div>
        <button type="submit" class="btn btn-primary">Iniciar Sesión</button>
      </form>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        email: '',
        password: ''
      }
    },
    methods: {
      submitLogin() {
        // Aquí puedes agregar tu lógica de autenticación
        alert(`Iniciando sesión con: ${this.email}`);
      }
    }
  }
  </script>
  