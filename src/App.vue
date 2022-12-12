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
          <cart-component
          :productos="productos" />
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
        <card-list-component
        :productos="productos"/>
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
  data() {
    return {
      productos: [
        {
          id: 1,
          marca: "Inti Zen",
          nombre: "Ilumine",
          img: "https://i.imgur.com/V0MO17C.png",
          descripcion:
            "Breakfast Tea que combina un té negro de Ceylon cosechado en altura y aire puro, con notas bien definidas de un té negro de Assam que le dan cuerpo, sabor y aroma a la taza.",
          precio: 254.45,
          stock: true,
          categoria: "Infusiones",
        },
        {
          id: 2,
          marca: "Inti Zen",
          nombre: "Inti Grey",
          img: "https://i.imgur.com/oja9ieW.png",
          descripcion:
            "Clásico Earl Grey sutilmente perfumado con bergamota, prensada a frío, que aporta notas cítricas a la base de té negro de Oriente. Cada taza es un encuentro con la tradición.",
          precio: 254.45,
          stock: true,
          categoria: "Infusiones",
        },
        {
          id: 3,
          marca: "Inti Zen",
          nombre: "Herbal Box",
          img: "https://i.imgur.com/BqxPzf3.png",
          descripcion:
            "Herbal Mix contiene la colección de las 4 tisanas de hierbas sin teína de Inti Zen, relajantes, digestivas y energizantes, para disfrutarlos a toda hora.",
          precio: 295.71,
          stock: true,
          categoria: "Infusiones",
        },
        {
          id: 4,
          marca: "Inti Zen",
          nombre: "Golden Chai",
          img: "https://i.imgur.com/shMffJD.png",
          descripcion:
            "Blend a base de cúrcuma, ligeramente picante y rico en antioxidantes. Mezclado con jengibre, canela y clavo, se convierte en el chai dorado perfecto.",
          precio: 284.16,
          stock: true,
          categoria: "Infusiones",
        },
        {
          id: 5,
          marca: "Inti Zen",
          nombre: "Dulce Manzanilla",
          img: "https://i.imgur.com/Hetn0WR.png",
          descripcion:
            "Flores de manzanilla relajantes con perfume de miel producen una tisana naturalmente dulce y suave, que irradia aromas duraderos y envolventes, con un toque cítrico de melisa.",
          precio: 284.16,
          stock: true,
          categoria: "Infusiones",
        },
        {
          id: 6,
          marca: "Inti Zen",
          nombre: "Tres Mentas",
          img: "https://i.imgur.com/1FT2CRo.png",
          descripcion:
            "La intensidad y frescura de las hojas de menta piperita egipcia, el toque dulce de la hierbabuena argentina y el aroma sensual de la menta silvestre andina.",
          precio: 284.16,
          stock: true,
          categoria: "Infusiones",
        },
        {
          id: 7,
          marca: "Inti Zen",
          nombre: "Inti Matcha",
          img: "https://i.imgur.com/1l4VTec.png",
          descripcion:
            "Té verde de Japón, Matcha, Yuzu cítrico y limón. Yuzu es un cítrico de origen japonés con sabor a fruta, similar al de una mandarina, y con aroma floral y dulce.",
          precio: 284.16,
          stock: true,
          categoria: "Infusiones",
        },
        {
          id: 8,
          marca: "Chocolate Colonial",
          nombre: "Para Taza",
          img: "https://i.imgur.com/HsbwBYI.png",
          descripcion:
            "El clásico chocolate en tabletas de 100gr para disfrutar de un buen desayuno y/o merienda. Chocolate semiamargo aromatizado con vainillina, libre de gluten, SIN TACC.",
          precio: 210.23,
          stock: true,
          categoria: "Chocolates",
        },
        {
          id: 9,
          marca: "Chocolate Colonial",
          nombre: "55% Cacao s/Azucar",
          img: "https://i.imgur.com/rkmzLIm.png",
          descripcion:
            "Sin agregado de azúcar. No es un alimento libre de azúcares, contiene azúcares propios de los ingredientes. No es un alimento reducido en calorías.",
          precio: 225.78,
          stock: true,
          categoria: "Chocolates",
        },
        {
          id: 10,
          marca: "Chocolate Colonial",
          nombre: "Organico 60% Cacao",
          img: "https://i.imgur.com/xNYatAN.png",
          descripcion:
            "Caja que contiene 10 unidades de 100 gramos. Peso neto 1 kg. Ingredientes: licor de cacao orgánico, azúcar orgánico, manteca de cacao orgánica.",
          precio: 516.23,
          stock: true,
          categoria: "Chocolates",
        },
        {
          id: 11,
          marca: "Chocolate Colonial",
          nombre: "Organico 70% Cacao",
          img: "https://i.imgur.com/0wSVdya.png",
          descripcion:
            "Caja que contiene 10 unidades de 100 gramos. Peso neto 1 kg. Ingredientes: licor de cacao orgánico, azúcar orgánico, manteca de cacao orgánica.",
          precio: 547.19,
          stock: true,
          categoria: "Chocolates",
        },
        {
          id: 12,
          marca: "Chocolate Colonial",
          nombre: "Organico 80% Cacao",
          img: "https://i.imgur.com/izXZhbN.png",
          descripcion:
            "Caja que contiene 10 unidades de 100 gramos. Peso neto 1 kg. Ingredientes: licor de cacao orgánico, azúcar orgánico, manteca de cacao orgánica.",
          precio: 597.25,
          stock: true,
          categoria: "Chocolates",
        },
        {
          id: 13,
          marca: "Chocolate Colonial",
          nombre: "Konfitt Almendras",
          img: "https://i.imgur.com/ebakCbT.png",
          descripcion:
            "Almendras cubiertas con chocolate blanco aromatizado con vainillina, libre de gluten. SIN TACC.",
          precio: 1463.19,
          stock: true,
          categoria: "Chocolates",
        },
        {
          id: 14,
          marca: "Chocolate Colonial",
          nombre: "Chocolatinas Semiamargas",
          img: "https://i.imgur.com/RE0SipS.png",
          descripcion:
            "Chocolatinas semiamargas Sin Tacc, de 5gr cada una. La presentación es en estuche de 50 unidades, peso neto 250g.",
          precio: 1358.24,
          stock: true,
          categoria: "Chocolates",
        },
        {
          id: 15,
          marca: "Cocoon",
          nombre: "Sin Azucar 1l",
          img: "https://i.imgur.com/c7aRuve.png",
          descripcion:
            "Bebida de almendras con verdadero sabor a almendras. Sin azúcar, sin saborizantes, sin aditivos artificiales. ¡Naturalmente rica!",
          precio: 255.78,
          stock: true,
          categoria: "Leches de Almendras",
        },
        {
          id: 16,
          marca: "Cocoon",
          nombre: "Original 1l",
          img: "https://i.imgur.com/4mczZwj.png",
          descripcion:
            "100% natural, de extractos vegetales. Nuestra bebida original es la alternativa saludable y liviana para agregarle a tu café o disfrutarla sola, tomala bien fría!",
          precio: 255.78,
          stock: true,
          categoria: "Leches de Almendras",
        },
        {
          id: 17,
          marca: "Cocoon",
          nombre: "Chocolatada 1l",
          img: "https://i.imgur.com/DTafSBu.png",
          descripcion:
            "Disfrutá del mejor sabor a chocolate intenso en nuestra chocolatada de almendras. Un sabor equilibrado y liviano para los amantes de lo dulce, y sin culpa!",
          precio: 278.25,
          stock: true,
          categoria: "Leches de Almendras",
        },
        {
          id: 18,
          marca: "Cocoon",
          nombre: "Coco 1l",
          img: "https://i.imgur.com/ab6dLSr.png",
          descripcion:
            "Nuestra bebida de coco es tan rica y naturalmente dulce que no necesitamos agregarle azúcar. Tomala sola, ¡bien fría! o sumala en tus licuados.",
          precio: 310.55,
          stock: true,
          categoria: "Leches de Almendras",
        },
        {
          id: 19,
          marca: "Cocoon",
          nombre: "Cajú 1l",
          img: "https://i.imgur.com/USP9wek.png",
          descripcion:
            "Nuestra bebida de castañas de cajú es tan rica y naturalmente dulce. Tomala sola, ¡bien fría! o sumala en tus licuados.",
          precio: 320.18,
          stock: true,
          categoria: "Leches de Almendras",
        },
        {
          id: 20,
          marca: "Cocoon",
          nombre: "Chocolatada 200ml",
          img: "https://i.imgur.com/zaZjblB.png",
          descripcion:
            "Disfrutá del mejor sabor a chocolate intenso en nuestra chocolatada de almendras. Un sabor equilibrado y liviano para los amantes de lo dulce, y sin culpa!",
          precio: 305.1,
          stock: true,
          categoria: "Leches de Almendras",
        },
        {
          id: 21,
          marca: "Cocoon",
          nombre: "Sin Azucar 200ml",
          img: "https://i.imgur.com/1gt0jLg.png",
          descripcion:
            "Bebida de almendras con verdadero sabor a almendras. Sin azúcar, sin saborizantes, sin aditivos artificiales. ¡Naturalmente rica!",
          precio: 330.57,
          stock: true,
          categoria: "Leches de Almendras",
        },
      ],
    };
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
