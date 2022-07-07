<template>
  <div id="app">
    <Header/>
    <div class="row">
      <div class="container">
        <div class="row">
          <div class="col" v-for="(producto, index) in productos" :key="index">
            <CardProducto :producto="producto" />
          </div>
        </div>
      </div>
    </div>
    
  </div>
</template>

<script>
import Header from './components/Header.vue'
import CardProducto from './components/CardProducto.vue'

export default {
  name: 'App',
  components: {
    Header, CardProducto
  },
  data() {
    return {
      productos: [
        {
          nombre: "Caramelera",
          precio: "$1000",
          imagen: "caramelera.jpg",
          descripcion: "Esta es una descripcion de una vela con envase",
        },
        {
          nombre: "Vela envase con tapa metal",
          precio: "$1500",
          imagen: "unavela.jpg",
          descripcion: "Esta es una descripcion de una vela con envase",
        },
        {
          nombre: "Difusor",
          precio: "$1400",
          imagen: "difusor.jpg",
          descripcion: "Esta es una descripcion de una vela con envase",
        },
        {
          nombre: "Esferas aromáticas",
          precio: "$500",
          imagen: "bolitas.jpg",
          descripcion: "Esta es una descripcion de una vela con envase",
        },
        {
          nombre: "carrusel",
          precio: "$1200",
          imagen: "carrusel.jpg",
          descripcion: "Esta es una descripcion de una vela con envase",
        },
        {
          nombre: "envase rojo",
          precio: "$1500",
          imagen: "velaroja.jpg",
          descripcion: "Esta es una descripcion de una vela con envase",
        },
      ],
    };
  },
}
</script>

<style>
#app {
  font-family: Montserrat, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
