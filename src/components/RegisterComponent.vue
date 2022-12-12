<template>
  <div>
    <h1 class="title-component">Registro</h1>
    <form class="registerFormComp">
      <div class="mb-3">
        <label for="registerName" class="form-label">Nombre</label>
        <input type="text" class="form-control" id="registerName" />
      </div>
      <div class="mb-3">
        <label for="registerLastName" class="form-label">Apellido</label>
        <input type="text" class="form-control" id="registerLastName" />
      </div>
      <div class="mb-3">
        <label for="registerEmail" class="form-label">Email</label>
        <input
          type="email"
          class="form-control"
          id="registerEmail"
          aria-describedby="emailHelp"
        />
      </div>
      <div class="mb-3">
        <label for="registerPassword" class="form-label">Password</label>
        <input type="password" class="form-control" id="registerPassword" />
      </div>
      <div class="mb-3">
        <label for="confirmRegisterPassword" class="form-label"
          >Confirmar Password</label
        >
        <input
          type="password"
          class="form-control"
          id="confirmRegisterPassword"
        />
      </div>
      <button type="submit" class="btn btn-primary btn-style">Registrarse</button>
      <p class="form-text mt-3">Ya estás Registrado? Ingresa desde <a href="#">aquí</a></p>
    </form>
  </div>
</template>

<script>
export default {
  name: "LoginComponent",
};
</script>

<style scoped>
.registerFormComp {
  border: 1px solid lightgrey;
  border-radius: 10px;
  padding: 2rem 4rem;
}

.form-text{
  font-size: .85rem;
}
.form-text a{
  text-decoration: none;
  color: lightsalmon;
  font-weight: 500;
}
</style>