<template>
  <div class="card-product my-3 my-md-1">
    <div class="container-info">
      <img :src="link" class="card-img-top" :alt="title" />
    </div>
    <div class="card-body">
      <div class="title-price">
        <h5 class="card-title text-center">{{ title }}</h5>
        <p class="category">({{ categoria }})</p>
        <p class="price">${{ precio }}</p>
      </div>
      <p class="descripcion card-text px-lg-5">
        {{ descripcion }}
      </p>
      <div class="buttons d-flex justify-content-around mt-3">
        <button class="btn btn-style btn-add" type="submit">Agregar</button>
        <button class="btn btn-style" type="submit">{{botonInfo}}</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardComponent",
  props: {
    link: String,
    title: String,
    descripcion: String,
    precio: Number,
    categoria: String,
    botonInfo: String
  },
};
</script>

<style scoped>
.card-product {
  width: 100%;
  position: relative;
  border: 1px solid lightgrey;
  border-radius: 7px;
  padding: 0 1rem 2rem;
  box-shadow: rgba(0, 0, 0, 0.35) 0px 3px 9px;
}
.card-product img {
  max-width: 200px;
  margin: 0 auto;
}
.card-title {
  font-family: Oswald;
  text-transform: uppercase;
  font-weight: 300;
  font-size: 1.3rem;
  margin-top: -3rem;
}
.descripcion {
  font-family: Roboto;
  font-weight: 300;
  font-size: 0.9rem;
}
.price {
  font-family: Oswald;
  font-size: 1.75rem;
  font-weight: 500;
  color: black;
}
.category {
  font-family: Roboto;
  font-size: 0.9rem;
  font-style: italic;
  text-transform: lowercase;
  margin: 0;
}

button.btn-style.btn-add{
    background-color: white;
    color: black;
}
button.btn-style.btn-add:hover{
    background-color: rgb(84, 194, 84);
    border-color: rgb(84, 194, 84);
    color: white;
}

/*///////////// Media Query ////////////*/
/* Desde 768px */
@media screen and (min-width: 767.98px) {
  .card-title {
    margin-top: 0;
    font-size: 1.4rem;
  }
}
</style>