<template>
  <div class="gridCardComponent">
    <card-component
      v-for="(producto, index) in productos"
      :key="index"
      :link="producto.img"
      :title="producto.nombre"
      :precio="producto.precio"
      :categoria="producto.categoria"
      :botonInfo="'Mas Info'"
      :productos="productos"
    />
  </div>
</template>

<script>
import CardComponent from './CardComponent.vue';

export default {
  name: "CardListComponent",
  props: {
    productos: Array
  },
  components: {
    CardComponent
  },

};
</script>

<style scoped>
.gridCardComponent {
  display: grid;
  grid-template-columns: .8fr;
  justify-content: center;
}


/*///////////// Media Query ////////////*/
/* Desde 576px */
@media screen and (min-width: 575.98px){
  .gridCardComponent{
    max-width: 80%;
    margin: 0 auto;
  }
}

/* Desde 768px */
@media screen and (min-width: 767.98px){
  .gridCardComponent{
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
    margin: 0;
    max-width: 100%;
  }
}

/* Desde 992px */
@media screen and (min-width: 991.98px){
  .gridCardComponent{
    margin: 0 auto;
    max-width: 80%;
  }
}

/* Desde 1280px */
@media screen and (min-width: 1279.98px){
  .gridCardComponent{
    grid-template-columns: repeat(4, 1fr);
    gap: 20px;
    margin: 0 auto;
    max-width: 100%;
  }
}
</style>