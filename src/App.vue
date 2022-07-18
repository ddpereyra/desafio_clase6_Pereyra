<template>
  <div id="app">
    <h1><u>Desafio Web Components</u></h1>
    <h3><i>Circuitos</i></h3>
    <FormularioRegistro 
      :nombre="nameCircuito"
      :rating="ratingCircuito"
      :limite="limiteCircuitos"
      :listado="circuitos"
    />
    <h3><i>Equipos</i></h3>
    <FormularioRegistro
      :nombre="nameEquipo"
      :rating="ratingEquipo"
      :limite="limiteEquipos"
      :listado="equipos" />
    <h3><i>Corredores</i></h3>
    <FormularioRegistro
      :nombre="nameCorredor"
      :rating="ratingCorredor"
      :limite="limiteCorredores"
      :listado="corredores" />
  </div>
</template>

<script>
/* eslint-disabled */
// import HelloWorld from './components/HelloWorld.vue'
import FormularioRegistro from './components/FormularioRegistro.vue'
export default {
  name: 'App',
  components: {
    // HelloWorld,
    FormularioRegistro
  },
  data() {
    const nameCircuito = ''
    const limiteCircuitos = 3
    const ratingCircuito = null
    const circuitos = [
        {
            id: 1,
            nombre: 'GP Argentina',
            fecha: '28/05/1986',
            rating: 6
        },
        {
            id: 2,
            nombre: 'GP Alemania',
            fecha: '13/12/1976',
            rating: 8
        },
        {
            id: 3,
            nombre: 'GP España',
            fecha: '05/11/1956',
            rating: 9
        }
    ]
    const nameEquipo = ''
    const limiteEquipos = 4
    const ratingEquipo = null
    const equipos = [
        {
            id: 1,
            nombre: 'Ferrari',
            fecha: '23/08/2000',
            rating: 2
        },
        {
            id: 2,
            nombre: 'Mercedes',
            fecha: '17/09/2001',
            rating: 3
        },
        {
            id: 3,
            nombre: 'Red Bull',
            fecha: '07/03/2007',
            rating: 1
        }
    ]
    const nameCorredor = ''
    const limiteCorredores = 5
    const ratingCorredor = null
    const corredores = [
        {
            id: 1,
            nombre: 'Leclerc',
            fecha: '02/06/1995',
            rating: 3
        },
        {
            id: 2,
            nombre: 'Hamilton',
            fecha: '12/01/1966',
            rating: 2
        },
        {
            id: 3,
            nombre: 'Verstappen',
            fecha: '10/09/1998',
            rating: 1
        }
    ]
    const tblstyle = { 'border': 'solid 1px' }
    return {
      nameCircuito,
      limiteCircuitos,
      ratingCircuito,
      circuitos,
      nameEquipo,
      limiteEquipos,
      ratingEquipo,
      equipos,
      nameCorredor,
      limiteCorredores,
      ratingCorredor,
      corredores,
      tblstyle
     }
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
