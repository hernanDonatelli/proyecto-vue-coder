<template>
  <div>
    <h1 class="loginTitle">Login</h1>
    <form class="loginFormComp">
      <div class="mb-3">
        <label for="loginEmail" class="form-label">Email</label>
        <input
          type="email"
          class="form-control"
          id="loginEmail"
          aria-describedby="emailHelp"
        />
      </div>
      <div class="mb-3">
        <label for="loginPassword" class="form-label">Password</label>
        <input type="password" class="form-control" id="loginPassword" />
      </div>
      <button type="submit" class="btn btn-primary">Login</button>
      <p class="form-text mt-3">No estás Registrado? Registrate <a href="#">aquí</a></p>
    </form>
  </div>
</template>

<script>
export default {
  name: "LoginComponent",
};
</script>

<style scoped>
.loginFormComp{
    border: 1px solid lightgrey;
    border-radius: 10px;
    padding: 2rem 4rem;
}
.loginTitle{
    font-family: Roboto;
    font-size: 2rem;
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