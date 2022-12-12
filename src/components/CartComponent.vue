<template>
  <div>
    <div class="container">
      <div class="row">
        <h1 class="title-component">Productos en Cart</h1>
        <div class="table-responsive">
          <table class="table cartTable">
            <thead>
              <tr>
                <th scope="col">id</th>
                <th scope="col">Nombre</th>
                <th scope="col">Marca</th>
                <th scope="col">Precio</th>
                <th scope="col">Info</th>
              </tr>
            </thead>
            <tbody>
              <fila-component
              is="fila-component"
              v-for="(producto, index) in cart"
              :key="index"
              :productos="productos"
              :id="producto.id"
              :nombre="producto.nombre"
              :marca="producto.marca"
              :precio="producto.precio"
              :info="producto.categoria"
              />
            </tbody>
          </table>
        </div>

        <button class="btn btn-style btn-cart" type="submit">Regresar</button>
      </div>
    </div>
  </div>
</template>

<script>
import FilaComponent from './FilaComponent.vue';

export default {
  name: "CartComponent",
  props: {
    productos: Array
  },
  components: {
    FilaComponent
  },
  data() {
    return {
      cart: [
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
          id: 15,
          marca: "Cocoon",
          nombre: "Sin Azucar 1l",
          img: "https://i.imgur.com/c7aRuve.png",
          descripcion:
            "Bebida de almendras con verdadero sabor a almendras. Sin azúcar, sin saborizantes, sin aditivos artificiales. ¡Naturalmente rica!",
          precio: 255.78,
          stock: true,
          categoria: "Leches de Almendras",
        }
      ]
    }
  },

};
</script>

<style scoped>
.cartTable {
  font-family: Roboto;
  font-size: 1rem;
}
.cartTable th{
  font-family: Oswald;
  font-size: 1.2rem;
  text-transform: uppercase;
  font-weight: 500;
}
.cartText {
  font-size: 0.85rem;
  margin: 1rem auto;
}
.btn-cart {
  max-width: 50%;
  margin: 0 auto;
}

/*///////////// Media Query ////////////*/
/* Desde 768px */
@media screen and (min-width: 767.98px){
  .btn-cart{
    max-width: 40%;
  }
}

/* Desde 992px */
@media screen and (min-width: 991.98px){
  .btn-cart{
    max-width: 30%;
  }
}

/* Desde 1280px */
@media screen and (min-width: 1279.98px){
  .btn-cart{
    max-width: 20%;
  }
}
</style>