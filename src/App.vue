<template>
  <div id="app">
    <div class="container">
      <!-- Formulario de Login -->
      <div class="row">
        <div class="loginForm col-12 mx-auto col-md-8 col-xl-6">
          <login-component />
        </div>
      </div>
      <!-- Formulario de registro -->
      <div class="row">
        <div class="registerForm my-5 col-12 mx-auto col-md-8 col-xl-6">
          <register-component />
        </div>
      </div>
      <!-- Carrito de compras -->
      <div class="row">
        <div class="cartComponent my-5 col-12 mx-auto">
          <cart-component />
        </div>
      </div>

      <!-- Producto individual -->
      <div class="row">
        <div class="cardComponent my-5 col-12 mx-auto col-sm-10 col-lg-7">
          <h1 class="title-component">Detalle de Producto</h1>
          <card-component
          :link="'https://i.imgur.com/V0MO17C.png'"
          :title="'Illumine'"
          :descripcion="'Breakfast Tea que combina un té negro de Ceylon cosechado en altura y aire puro, con notas bien definidas de un té negro de Assam que le dan cuerpo, sabor y aroma a la taza.'"
          :precio="254.47"
          :categoria="'Infusiones'"
          :botonInfo="'Volver'"/>
        </div>
      </div>

      <!-- Grilla de productos -->
      <div class="row">
        <h1 class="title-component m-0">Productos en stock</h1>
        <card-list-component />
      </div>
    </div>
  </div>
</template>

<script>
import LoginComponent from "./components/LoginComponent.vue";
import RegisterComponent from "./components/RegisterComponent.vue";
import CartComponent from "./components/CartComponent.vue";
import CardComponent from "./components/CardComponent.vue";
import CardListComponent from "./components/CardListComponent.vue";

export default {
  name: "App",
  components: {
    LoginComponent,
    RegisterComponent,
    CartComponent,
    CardComponent,
    CardListComponent
  },

};
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
h1.title-component {
  font-family: Roboto;
  font-size: 1.8rem;
  font-weight: 400;
}
button.btn.btn-style {
  font-family: Oswald;
  text-transform: uppercase;
  font-weight: 300;
  font-size: 1.1rem;
  background-color: black;
  border: 1px solid black;
  color: white;
  padding: 0.3rem 1.25rem;
}
button.btn.btn-style:hover {
  background-color: white;
  color: black;
}

/*///////////// Media Query ////////////*/
/* Desde 992px */
@media screen and (min-width: 991.98px){
  button.btn.btn-style{
    padding: .3rem 2rem;
  }
}

/* Desde 1280px */
@media screen and (min-width: 1279.98px){
  button.btn.btn-style{
    padding: .3rem 1.5rem;
  }
}
</style>
