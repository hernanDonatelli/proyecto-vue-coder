<template>
    <tr>
      <td>{{ id }}</td>
      <td>{{ nombre }}</td>
      <td>{{ marca }}</td>
      <td>${{ precio }}</td>
      <td>{{ info }}</td>
    </tr>
</template>

<script>
export default {
  name: "FilaComponente",
  props: {
    id: Number,
    nombre: String,
    marca: String,
    precio: Number,
    info: String,
  },
};
</script>

<style scoped>
</style>