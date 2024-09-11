<template>
  <div class="container mt-4">
    <!-- Captura el evento "user-registered" emitido desde UserForm -->
    <user-form @user-registered="addUser" />
    <user-table :users="users" />
  </div>
</template>

<script>
import UserForm from './components/UserForm.vue';
import UserTable from './components/UserTable.vue';

export default {
  components: {
    UserForm,
    UserTable
  },
  data() {
    return {
      users: []
    };
  },
  methods: {
    addUser(newUser) {
      // Agregar el nuevo usuario a la lista de usuarios
      this.users.push(newUser);
    }
  }
};
</script>

<style scoped>
</style>
