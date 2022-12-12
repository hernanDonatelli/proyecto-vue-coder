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
              <tr>
                <td colspan="5">
                  <p class="cartText text-center w-100">
                    No hay productos ingresados aún.
                  </p>
                </td>
              </tr>
            </tbody>
          </table>
        </div>

        <button class="btn btn-style btn-cart" type="submit">Regresar</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CartComponent",
};
</script>

<style scoped>
.cartTable {
  font-family: Roboto;
  font-size: 1rem;
}
.cartTable th{
  font-family: Oswald;
  text-transform: uppercase;
  font-weight: 400;
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