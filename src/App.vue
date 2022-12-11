<template>
  <div id="app">
    <div class="container">
      <div class="row">
        <div class="loginForm col-12 mx-auto col-md-8 col-xl-6">
          <login-component />
        </div>
      </div>
      <div class="row">
        <div class="registerForm my-5 col-12 mx-auto col-md-8 col-xl-6">
          <register-component />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import LoginComponent from './components/LoginComponent.vue';
import RegisterComponent from './components/RegisterComponent.vue';

export default {
  name: 'App',
  components: {
    LoginComponent,
    RegisterComponent
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
